# QuantActions for Developers - QA Android SDK

The QuantActions SDK for Android enables a developer to add all the QuantActions functionalities to an android app. This includes:

- Automatic data collection
- Access processed measures and insights from QA Analytics
- Enabling device communication
- Participate in different programs

The QuantActions SDK for Android can be set up with a few easy steps. QA recommends the use of `gradle` as build tool and of Android Studio as IDE for the development and provides example code for both Java and Kotlin.

---

## Android Studio Setup

1. Ensure that you have selected a minimum Android SDK of **16** for your project by checking that the `app`-level `build.gradle` file contains this code

```Java
defaultConfig {
    minSdkVersion 16
}
```

2. Add the QA SDK dependency to your Project by adding the following lines to your project-level `build.gradle` file

```Java
allprojects {
    repositories {
        maven { url 'https://dl.bintray.com/qa/maven' }
    }
}
```

3. Add the QA SDK dependency to your `app`-level `build.gradle` file

```Java
implementation 'com.quantactions.sdk:qa_sdk_trial:1.0'
```

and re-sync the project. Remember to check the [QA SDK webpage](https://bintray.com/beta/#/qa/maven/android-trial-sdk) for the latest SDK version in case you are reading an old version of the documentation.

4. Done! You are now ready to start adding QA functionality to your code.

----

## Adding QA functionality to an app

The whole QA functionality can be accessed everywhere in the code by the singleton `QA` that can be instantiate like this.

```Java
// Java
import com.quantactions.sdk_trial.QA;
...

QA qa = QA.getInstance();
```

```kotlin
// Kotlin
import com.quantactions.sdk_trial.QA;

...

val qa: QA = QA.getInstance()
```

Before using any functionality, the QA singleton needs to be initialized. To do you will need an `access token` provided by QuantActions. If you have not yet received your `access token` please [contact us](mailto:development@quantactions.com).

Once in possession of the `access_token`, the simplest thing to do is to create a `string` resource in the `res/values/strings.xml` file to reference the access token. This makes it easier to change the token if it were to change.

```xml
<string name="access_token">your_access_token_here</string>
```

Once you have that, you can check that the `access token` is correct and everything works as it is supposed to by using the method `validateToken` in the following way.

```Java
qa.validateToken(context, getString(R.string.access_token), null);
```

The significance fo the last element, now set to `null` will be covered in a later chapter on QA Runnables

---

QA Runnables
------------
In almost all the public functions of the singleton QA, you will find that they accept an object that should implements the basic QARunnable interface.
Since most of what QA does is asynchronous, this allows developers to infuse delayed behavior when a task succeeds or when a task fails (for example if connection is not available).
The QA SDK offers an example of a basic objects that implements the QA runnable interface QARunnableExample.    
