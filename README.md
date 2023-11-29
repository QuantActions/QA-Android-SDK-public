#Module SDK

![version](https://img.shields.io/badge/version-0.9.2-blue)

The QuantActions SDK for Android enables a developer to add all the QuantActions functionalities to an android app. This includes:

- Automatic data collection
- Access processed metrics and insights from the Tap Intelligence Engine (TIE)
- Enabling device communication
- Subscribe to different cohorts

The QuantActions SDK for Android can be set up with a few easy steps. We recommend the use of `gradle` as build tool and of Android Studio as IDE for the development.

This is an issue-only public repository for the distribution of the documentation of the SDK, the gathering of issues and feature requests and the distribution of samples.


## 1. Android Studio setup

The SDK is distributed via [JitPack](https://jitpack.io/), for now the SDK is private and can only be accessed prior a request, please write you request (containing your **github username**) to [development@quantactions.com](mailto:development@quantactions.com).

1. Ensure that you have selected a minimum Android SDK of **21** for your project by checking that the app-level `build.gradle`, also we recommend using JAVA 11, remember to enable desugaring options since the SDK uses advanced Java functionality that are not normally available at lower Android API levels

    ```groovy
   android {
    defaultConfig {
        minSdkVersion 21
    }
   
    compileOptions {
        coreLibraryDesugaringEnabled true
        sourceCompatibility JavaVersion.VERSION_11
        targetCompatibility JavaVersion.VERSION_11
     }
     kotlinOptions {
        jvmTarget = JavaVersion.VERSION_11.toString()
     }
   }
   
   dependencies {
       coreLibraryDesugaring 'com.android.tools:desugar_jdk_libs:2.0.3'
   }
   
    ```

2. Follow the [instructions from JitPack](https://jitpack.io/docs/PRIVATE/) for the access to private artifacts. When you have your auth token simply add it you your general `gradle.properties`

    ```groovy
    authToken=api_key_from_jitpack
    ```

   and add the JitPack repo to the project-level `build.gradle` or the `seetings.gradle` depending of your project setup

    ```groovy
    maven {
       url "https://jitpack.io"
       credentials { username authToken }
    }
    ```

3. Add the QA SDK dependency to your app-level `build.gradle` file

    ```groovy
    implementation 'com.github.QuantActions:QA-Android-SDK:0.9.2'
    ```

   and re-sync the project. Remember to check the latest SDK version in case you are reading an old version of the documentation.

4. Done! You are now ready to start adding QA functionality to your code.

----

## 2. Adding QA functionality to an app

The whole QA functionality can be accessed everywhere in the code by the singleton `QA` that can be instantiate like this.

```kotlin
import com.quantactions.sdk.QA
val qa = QA.getInstance(context)
```

Before using any functionality, the QA singleton needs to be initialized. To do so you will need an `api_key` provided by QuantActions. If you have not yet received your `api_key` please [contact us](mailto:development@quantactions.com).

Once in possession of the `api_key`, the simplest thing to do is to add your `api_key` to the app-level `build.gradle`

 ```groovy
 android {
    compileSdkVersion 31

    defaultConfig {
        minSdkVersion 21
        buildConfigField("String", "QA_API_KEY", "\"api_key\"")
    }
  }
 ```

then you can access it in the code to initialize the SDK.

```kotlin
qa.init(context,
        apiKey=BuildConfig.QA_API_KEY,
        basicInfo=BasicInfo(
        age=1985, 
        gender=QA.Gender.UNKNOWN, 
        selfDeclaredHealthy=true))
```

------------------------

## 3. Request the permissions

For the SDK to work properly, the app that uses it needs to request 2 permissions:
- OVERLAY PERMISSION: `Settings.ACTION_MANAGE_OVERLAY_PERMISSION`
- USAGE ACCESS: `Settings.ACTION_USAGE_ACCESS_SETTINGS`

To prompt the user to enable these permissions you can use the methods

```kotlin
qa.requestOverlayPermission(context) // opens overlay settings page
qa.requestUsagePermission(context) // opens usage settings page
```

Since these permissions can be revoked at any time by the user, it is important to routinely check
that they are granted, to do so the easiest way is to have background scheduled task that check that the permissions are granted
using `qa.canUsage(context)` and `qa.canDraw(context)` and fire a notification in case the permissions have been lost.

-----

## 4. Sign-up to a cohort
To track a device it is **necessary** to subscribe the device to a cohort. Each device can be subscribed in two ways. For a cohort with a known number of devices to track, QuantActions provides a set of codes (subscriptionIds) of the form `138e...28eb` that have to be distributed. The way the code is entered into the app is the choice of the developer. In our TapCounter R&D app we use both a copy&paste method and a QR code scanning method, once the code as been acquired the device can then be registered using the SDK

```kotlin
qa.subscribe(subscriptionId)
```   

where `subscriptionId` is the string corresponding to the subscription ID.

For cohorts where the number of participants is unknown the SDK can be used to register the device by simply using the `cohortId` provided by QA (this way needs special access so make sure you are authorized by QuantActions to use this functionality).

```kotlin
qa.subscribe(cohortId)
```   

Note that multiple devices can be subscribed using the same `subscriptionId`, this is the case when a user has multiple devices or changes devices (e.g. old phone is broken).
The data from multiple devices sharing the same `subscriptionId` will be merged to generate insights and metric, thus the same `subscriptionId` should not be used for different users.
When subscribing the device using a general `cohortId`, get device gets automatically assigned a `subscriptionId`, to retrieve this id and use it to register other devices one case use the following code.

```kotlin
qa.getSubscriptionId(applicationContext).collect {
    when(it) {
        is QAResponse.QASuccessResponse -> {
           Timber.d(it.data!!.subscriptionId)
        }
        is QAResponse.QAErrorResponse -> {
            if (it.message!!.contains("it is not part of any cohort")){
                Timber.d("Device is registered but not part of any cohort")
            } else {
               Timber.d("Device is NOT registered with QA backend")
            }
        }
        is QAResponse.QALoadingResponse -> Timber.d("Loading")
    }
}
```

---

## 5. Firebase

For the best experience with the SDK we strongly recommend to add to your app [Firebase Messaging, Crashlytics and Analytics](https://firebase.google.com/), this will allow QA service to also communicate with the app to check its status and more.

------------------

## 6. The notification icon
Because QA SDK is always active in the background, Android API O and above require a notification to always be present to inform the user, by default the notification uses [this](https://fonts.google.com/icons?selected=Material%20Icons%20Outlined%3Aequalizer%3A) icon. To override it and use your own icon you can simply create a drawable named `ic_equalizer_black_24dp` and place it in your `res/drawable` folder and this will override the drawable of the SDK.

Moreover the SDK notification uses a separate notification channel called `QA Service` and can be easily unselected by the user from the OS notifications settings to avoid having it always present.


-------

## 7. TL:DR
Minimal example

- Get a `QA_API_KEY` from [QuantActions](mailto:development@quantactions.com)
- Get a `QA_COHORT_ID` from [QuantActions](mailto:development@quantactions.com)
- Get a `authToken` from [Jitpack](https://Jitpack.io)


`gradle.properties` (global)

```groovy
authToken=api_key_from_jitpack
```


`build.gradle` (project level)

```groovy
allprojects {
    repositories {
        google()
        jcenter()
        maven { url "https://jitpack.io"
            credentials { username authToken }
        }
    }
}

```

`build.gradle` (app level)

```groovy
android {
   defaultConfig {
      minSdkVersion 21
      buildConfigField("String", "QA_API_KEY", "\"api_key\"")
      buildConfigField("String", "QA_COHORT_ID", "\"cohort_id\"")
   }

   compileOptions {
      coreLibraryDesugaringEnabled true
      sourceCompatibility JavaVersion.VERSION_11
      targetCompatibility JavaVersion.VERSION_11
   }
   kotlinOptions {
      jvmTarget = JavaVersion.VERSION_11.toString()
   }
}

dependencies {
   coreLibraryDesugaring 'com.android.tools:desugar_jdk_libs:2.0.3'
}

```

`MainActivity.kt`

```kotlin
package com.example.sdktestapp

import android.os.Bundle
import androidx.appcompat.app.AppCompatActivity
import androidx.lifecycle.lifecycleScope
import com.quantactions.sdk.BasicInfo
import com.quantactions.sdk.QA
import com.quantactions.sdktestapp.BuildConfig.QA_API_KEY
import com.quantactions.sdktestapp.BuildConfig.QA_COHORT_ID
import kotlinx.coroutines.ExperimentalCoroutinesApi
import kotlinx.coroutines.launch

class MainActivity : AppCompatActivity() {

    @ExperimentalCoroutinesApi
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        // Get QA singleton
        val qa = QA.getInstance(this@MainActivity)

        lifecycleScope.launch {
            qa.init(this@MainActivity, QA_API_KEY, BasicInfo(1985, QA.Gender.UNKNOWN, false)) // initialize SDK
            qa.requestOverlayPermission(MainActivity.this) // opens overlay settings page
            qa.requestUsagePermission(MainActivity.this) // opens usage settings page
            qa.subscribe(QA_COHORT_ID)  // register the device with the backend
            qa.syncData(this@MainActivity) // optional: sync the data
        }
    }
}
```

---

## 8. Checking that everything is running fine
After the integration of the SDK has been done, you can add some checks to make sure everything is running fine.
1. You can can check that device is registered with the backend by using `qa.isDeviceRegistered(context)` (returns a bool)
2. You can check that the data collection is running fine by using `qa.isDataCollectionRunning(context)` (returns a bool)
3. You can check that the registration to a cohort was successful
```kotlin
    viewModelScope.launch {
        withContext(Dispatchers.IO) {
            val subscription = qa.subscription()
            if (subscription != null) {
                Timber.d("Device is registered with cohort ${subscription.cohortId}")
            } else {
                Timber.d("Device is NOT registered with any cohort")
            }
        }
    }
```

## 9. Pausing data collection

Although we do not recommend it, the data collection can be paused/resumed via the methods offered by QA singleton
[qa.pauseDataCollection(context)](com.quantactions.sdk.QA.pauseDataCollection) and [qa.resumeDataCollection(context)](com.quantactions.sdk.QA.resumeDataCollection)

## 10. Metrics and Trends retrieval
While the data collection and synchronization is automated within the SDK. Retrieval of metrics and insights
has to be done manually within the app in order to access only the subset of metrics and trends that the application needs.

The metrics and trends can be retrieve programmatically in the following way:

```kotlin
qa.getMetric(Metric.SLEEP_SCORE)
qa.getMetric(Trend.SLEEP_SCORE)
qa.getMetric(Metric.COGNITIVE_FITNESS)
qa.getMetric(Trend.COGNITIVE_FITNESS)
```

Check [Metrics](com.quantactions.sdk.Metric) and [Trends](com.quantactions.sdk.Trend) for the list of
metrics and trends available in the current version of the SDK

The function returns an asynchronous [Kotlin Flow](https://kotlinlang.org/docs/flow.html) containing a
[TimeSeries](com.quantactions.sdk.TimeSeries) object.
The test app accompanying the SDK has some examples on how to handle the return data.

Since the metrics for a user take from 2 to 7 days to be available (see [ETA](com.quantactions.sdk.Metric.eta)).
Developer can have access to sample metrics (that update every day) from a sampled device with [getMetricSample](com.quantactions.sdk.QA.getMetricSample)

## 11. Metrics and Trends description

### 11.1. Metrics

The current version is shipped with the following metrics:

- [SLEEP_SCORE](com.quantactions.sdk.Metric.SLEEP_SCORE), [COGNITIVE_FITNESS](com.quantactions.sdk.Metric.COGNITIVE_FITNESS), [SOCIAL_ENGAGEMENT](com.quantactions.sdk.Metric.SOCIAL_ENGAGEMENT):
  Each of these metric has a value in the range 0-100 and is shipped with confidence intervals (high and low)
  and a general confidence about the metric.

- [SLEEP_SUMMARY](com.quantactions.sdk.Metric.SLEEP_SUMMARY): This metric reports more information about the sleep of the user including bed time, wake up time
  and number and length of interruptions. See also [SleepSummary](com.quantactions.sdk.data.model.SleepSummary)
  for more information on how this metric is organized.

- [SCREEN_TIME_AGGREGATE](com.quantactions.sdk.Metric.SCREEN_TIME_AGGREGATE): This metric contains the total screen time as well as the screen time for social app, see also [ScreenTimeAggregate](com.quantactions.sdk.data.model.ScreenTimeAggregate)

- [ACTION_SPEED](com.quantactions.sdk.Metric.ACTION_SPEED): This metric is reported in milliseconds and refers to the amount of time it takes for the user to decide and complete a task on their smartphone.
- [TYPING_SPEED](com.quantactions.sdk.Metric.TYPING_SPEED):This metric is reported in milliseconds and represents the time efficiency of the user in typing any kind of text on their smartphone.
- [SOCIAL_TAPS](com.quantactions.sdk.Metric.SOCIAL_TAPS): This metrics report the number of taps on social apps.


### 11.2. Trends

The trends objects are TimeSeries that hold the daily values of the trend. For each day you get a
short (2 weeks), medium (6 weeks) and long (1 year) trend.

- [COGNITIVE_FITNESS](com.quantactions.sdk.Trend.COGNITIVE_FITNESS)
- [ACTION_SPEED](com.quantactions.sdk.Trend.ACTION_SPEED)
- [TYPING_SPEED](com.quantactions.sdk.Trend.TYPING_SPEED)
- [SLEEP_SCORE](com.quantactions.sdk.Trend.SLEEP_SCORE)
- [SLEEP_LENGTH](com.quantactions.sdk.Trend.SLEEP_LENGTH)
- [SLEEP_INTERRUPTIONS](com.quantactions.sdk.Trend.SLEEP_INTERRUPTIONS)
- [SOCIAL_ENGAGEMENT](com.quantactions.sdk.Trend.SOCIAL_ENGAGEMENT)
- [SOCIAL_SCREEN_TIME](com.quantactions.sdk.Trend.SOCIAL_SCREEN_TIME)
- [SOCIAL_TAPS](com.quantactions.sdk.Trend.SOCIAL_TAPS)
- [THE_WAVE](com.quantactions.sdk.Trend.THE_WAVE)

The [TrendHolder](com.quantactions.sdk.data.model.TrendHolder) contains 9 values. For each time
resolution (short, medium, long) the trend has 3 values:
- `differenceXYZ`: is the amount the metric has increased decrease (note: it is reported in the same unit as the metric)
- `statisticXYZ`: is the p-value of the test done to check if the trend is significant (generally this can be safely ignored)
- `significanceXYZ`: is the significance of the trend, +1 means metric has significantly increase, -1 means metric has significantly decreased, 0 means no significant change

While the metrics and trends have daily resolutions, they are updated every two hours.

In some cases the metrics for a day might be missing, in that case it means that there was not enough
data collect for that day to give an estimate or that the confidence was too low to give an appropriate estimate.
When some days are missing you can fill in the gaps with NaNs using [fillMissingDays](com.quantactions.sdk.TimeSeries.fillMissingDays)

Checkout the metrics individual pages for more information about each metric.

## 12. Journaling

The SDK allows also to use a journaling function to log a series of entries. Each entry is composed of:
- A date
- A small text describing the entry
- A list of events (from a predefined pool)
- A rating (1 to 5) for each event in the entry

The predefined [events](com.quantactions.sdk.data.entity.JournalEvent) can be retrieved with [getJournalEvents](com.quantactions.sdk.QA.getJournalEvents).
With that adding an entry is done by using [createJournalEntry](com.quantactions.sdk.QA.createJournalEntry).

Entries can also be [deleted](com.quantactions.sdk.QA.deleteJournalEntry).

The full journal (all entries) can be retrieved with [getJournal](com.quantactions.sdk.QA.getJournal)

As for the metrics an example journal can be retrieved for debug purposes with [getSampleJournal](com.quantactions.sdk.QA.getSampleJournal).

## 13. Questionnaires

Both classic and custom questionnaires can be subministered to users via the SDK.
Get in touch [with us](mailto:development@quantactions.com) for more information about this feature.

## 14. Issue tracking and contact
Feel free to use the issue tracking of this repo to report any problem with the SDK, in case of more immediate assistance need feel free to contact us at [development@quantactions.com](mailto:development@quantactions.com)

---

#Package com.quantactions.sdk
The main functionality of the Quantactions Android SDK.

#Package com.quantactions.sdk.data.entity
Entities used across the SDK for particular functionalities.

#Package com.quantactions.sdk.model
Data models used across the SDK for particular functionalities.

#Package com.quantactions.sdk.exceptions
Exceptions that the SDK might be throwing.



