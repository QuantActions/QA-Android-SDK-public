# QuantActions for Developers - QA Android SDK

The QuantActions SDK for Android enables a developer to add all the QuantActions functionalities to an android app. This includes:

- Automatic data collection
- Access processed measures and insights from QA Analytics
- Enabling device communication
- Participate in different programs

The QuantActions SDK for Android can be set up with a few easy steps. We recommend the use of `gradle` as build tool and of Android Studio as IDE for the development.

This is an issue-only public repository for the distribution of the documentation of the QA SDK and the gathering of issues. The documentation can be read [here](./docs/index.md) in GitHub-flavoured markdown, you can also download this repo and locally access the [HTML](./htmldocs) version if you prefer.

---

## 1. Android Studio Setup

The SDK is distributed via [JitPack](https://jitpack.io/), for now the SDK is private and can only be accessed prior a request, please write you request (containing your github username) to [development@quantactions.com](mailto:development@quantactions.com).

1. Ensure that you have selected a minimum Android SDK of **21** for your project by checking that the app-level `build.gradle` file contains this code

``` Java
defaultConfig {
    minSdkVersion 21
}
```

2. Follow the [instructions from JitPack](https://jitpack.io/docs/PRIVATE/) for the access to private artifacts. when you have your auth token simply add it you your general `gradle.properties`

```
authToken=auth_token_from_jitpack
```

and add the JitPack repo to the project-level `build.gradle`

``` Java
...
allprojects{
  repositories {
      maven {
          url "https://jitpack.io"
          credentials { username authToken }
      }
  }
}
...
```

3. Add the QA SDK dependency to your app-level `build.gradle` file

``` Java
implementation 'com.github.QuantActions:QA-Android-SDK:0.5.0'
```

and re-sync the project. Remember to check the latest SDK version in case you are reading an old version of the documentation.

4. Done! You are now ready to start adding QA functionality to your code.

----

## 2. Adding QA functionality to an app

The whole QA functionality can be accessed everywhere in the code by the singleton `QA` that can be instantiate like this.

``` Java
import com.quantactions.sdk.QA;
...

QA qa = QA.getInstance();
```

Before using any functionality, the QA singleton needs to be initialized. To do so you will need an `auth_token` provided by QuantActions. If you have not yet received your `auth_token` please [contact us](mailto:development@quantactions.com).

Once in possession of the `auth_token`, the simplest thing to do is to create a `string` resource in the `res/values/strings.xml` file to reference the access token.

```xml
<string name="auth_token">your_access_token_here</string>
```

Once you have that, you can check that the `auth_token` is correct and everything works as it is supposed to by using the method `validateToken` in the following way.

``` Java
qa.validateToken(context, getString(R.string.access_token));
```

Finally you can initialize the SDK

``` Java
qa.init(context, getString(R.string.access_token), null);
```

While the above setup is good for debugging, we suggest to use a slightly different setup for production to avoid leaving the `auth_token` in clear in the string resources.

 For a better setting, add your `auth_token` to the app level `build.gradle`

 ``` Java
 android {
    compileSdkVersion 31

    defaultConfig {
        minSdkVersion 21
        ...
        buildConfigField("String", "QA_AUTH_KEY", "\"auth_token\"")
    }
    ...
  }
 ```

 then you can access it in the code, for example to initialize the SDK.

 ``` Java
 qa.init(context, BuildConfig.QA_AUTH_KEY, null);
 ```


------------------------

## 3. Request the permissions

For the SDK to work properly, the app that uses it needs to request 2 permissions:
- OVERLAY PERMISSION: `Settings.ACTION_MANAGE_OVERLAY_PERMISSION`
- USAGE ACCESS: `Settings.ACTION_USAGE_ACCESS_SETTINGS`

To prompt the user to enable these permissions you can use the methods

``` Java
qa.requestOverlayPermission(context) // opens overlay settings page

qa.requestUsagePermission(context) // opens usage settings page
```

-----

## 4. Signup to a study
To track a device it is **necessary** to subscribe the device to a cohort (also called study). Each device can be subscribed in two ways. For a study with a known number of devices to track, QuantActions provides a set of codes of the form `138e...28eb` that have to be distributed. The way the code is entered into the app is the choice of the developer. In our TapCounter R&D app we use both a copy&paste method and a QR code scanning method, once the code as been acquired the device can the registered using the SDK

``` Java
qa.signUpForStudy(context, participationId, null));
```   

where `participationId` is the string corresponding to the participation ID and the `null` can be substituted by any class that implements the QARunnable interface (e.g. SnackRun).

For cohorts (or studies) where the number of participants is unknown the SDK can be used to register the device by simply using the `studyId` provided by QA (this way needs special access so mae sure you are authorized by QuantActions to use this functionality).

``` Java
qa.signUpForStudy(context, studyId, null));
```   

---

## Firebase

For the best experience with the SDK we strongly recommend to add to your app [Firebase Messaging, Crashlytics and Analytics](https://firebase.google.com/), this will allow QA service to also communicate with the app to check its status and more.

------------------


## The notification icon
Because QA SDK is always active in the background, Android API O and above require a notification to always be present to inform the user, by default the notification uses [this](https://fonts.google.com/icons?selected=Material%20Icons%20Outlined%3Aequalizer%3A) icon. To override it and use your own icon you can simply create a drawable named `ic_equalizer_black_24dp` and place it in your `res/drawable` folder and this will override the drawable of the SDK.

Moreover the SDK notification uses a separate notification channel called `QA Service` and can be easily unselected from the OS notifications settings to avoid having it always present.  


-------

# TL:DR
Minimal example

- Get a `QA_AUTH_KEY` from [QuantActions](mailto:development@quantactions.com)
- Get a `QA_STUDY_ID` from [QuantActions](mailto:development@quantactions.com)
- Get a `authToken` from [Jitpack](https://Jitpack.io)


`gradle.properties` (global)

```
authToken=auth_token_from_jitpack
```


`build.gradle` (project level)

``` Java
...
allprojects {
    repositories {
        google()
        jcenter()
        maven { url "https://jitpack.io"
            credentials { username authToken }
        }
    }
}
...
```

`build.gradle` (app level)

``` Java
implementation 'com.github.QuantActions:QA-Android-SDK:0.5.0'

```


`MainActivity.java`

``` Java
package com.example.sdktestapp

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import com.quantactions.sdk.QA
import com.example.sdktestapp.BuildConfig.QA_AUTH_KEY
import com.example.sdktestapp.BuildConfig.QA_STUDY_ID

public class MainActivity extends AppCompatActivity {
  @Override
  protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        QA qa = QA.getInstance() // instantiate
        qa.init(MainActivity.this, QA_AUTH_KEY, 1991, 2) // initialize SDK
        qa.requestOverlayPermission(MainActivity.this) // opens overlay settings page
        qa.requestUsagePermission(MainActivity.this) // opens usage settings page
        qa.signUpForStudy(MainActivity.this, QA_STUDY_ID));  // register the device with the backend
        qa.syncData(MainActivity.this) // optional: sync the data
    }
}
```

---

## Data retrieval 
While the data collection and synchronization is automated within the SDK. Retrieval of processed 
metrics has to be done manually within the app in order to access only the subset of metrics that the application needs.

There are 2 types of Metrics:
- numerical values (e.g. sleep score for Tuesday = 80.9)
- string values (e.g. total screen time for Tuesday = 2:20 in the format [hh:mm])

The metrics can be retrieve programmatically in the following way:

``` Java
getStat(context, statCode);
getStat(context, statCode);
```

Both functions return an asynchronous [Kotlin Flow](https://kotlinlang.org/docs/flow.html).
The test app accompanying the SDK has some examples on how to handle the return data.

Regarding `statCode`, you will receive a list of Metrics and corresponding codes from us depending 
on what metrics you have requested.

---

## Issue tracking and contact  
Feel free to use the issue tracking of this repo to report any problem with the SDK, in case of more immediate assistance need feel free to contact us at [development@quantactions.com](mailto:development@quantactions.com)
