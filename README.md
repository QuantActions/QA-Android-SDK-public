# QuantActions for Developers - QA Android SDK

The QuantActions SDK for Android enables a developer to add all the QuantActions functionalities to an android app. This includes:

- Automatic data collection
- Access processed measures and insights from QA Analytics
- Enabling device communication
- Participate in different programs

The QuantActions SDK for Android can be set up with a few easy steps. We recommend the use of `gradle` as build tool and of Android Studio as IDE for the development and provides example code for both Java and Kotlin.

This is an issue-only public repository for the distribution of the documentation of the QA SDK and the gathering of issues. The documentation can be read [here](./docs/README.md) in GitHub-flavoured markdown, you can also download this repo and locally access the [HTML](./htmldocs) version if you prefer.

---

## Android Studio Setup

The SDK is distributed via [JitPack](https://jitpack.io/), for now the SDK is private and can only be accessed prior a request, please write you request (containing your github username) to [development@quantactions.com](emailto:development@quantactions.com).

1. Ensure that you have selected a minimum Android SDK of **16** for your project by checking that the app-level `build.gradle` file contains this code

```Java
defaultConfig {
    minSdkVersion 16
}
```

2. Follow the [instructions from JitPack](https://jitpack.io/docs/PRIVATE/) for access private artifacts. when you have your auth token simply add it you your general `gradle.properties` and the JitPack repo to the project-level `build.gradle`

```
repositories {
    maven {
        url "https://jitpack.io"
        credentials { username authToken }
    }
}
```

3. Add the QA SDK dependency to your app-level `build.gradle` file

```Java
implementation 'com.github.QuantActions:QA-Android-SDK:0.4.0'
```

and re-sync the project. Remember to check the latest SDK version in case you are reading an old version of the documentation.

4. Done! You are now ready to start adding QA functionality to your code.

----

## Adding QA functionality to an app

The whole QA functionality can be accessed everywhere in the code by the singleton `QA` that can be instantiate like this.

```Java
// Java
import com.quantactions.sdk.QA;
...

QA qa = QA.getInstance();
```

```kotlin
// Kotlin
import com.quantactions.sdk.QA;

...

val qa: QA = QA.getInstance()
```

Before using any functionality, the QA singleton needs to be initialized. To do so you will need an `auth_token` provided by QuantActions. If you have not yet received your `auth_token` please [contact us](mailto:development@quantactions.com).

Once in possession of the `auth_token`, the simplest thing to do is to create a `string` resource in the `res/values/strings.xml` file to reference the access token.

```xml
<string name="auth_token">your_access_token_here</string>
```

Once you have that, you can check that the `auth_token` is correct and everything works as it is supposed to by using the method `validateToken` in the following way.

```Java
qa.validateToken(context, getString(R.string.access_token), null);
```

The significance fo the last element, now set to `null` will be covered in a later chapter on QA Runnables

Finally you can initialize the sdk

```Java
qa.init(context, getString(R.string.access_token), null);
```

While the above setup is good for debugging, we suggest to use a slightly different setup for production to avoid leaving the `auth_token` in clear in the string resources.

 For a better setting, add your `auth_token` to the app level `build.gradle`

 ```Java
 android {
    compileSdkVersion 31

    defaultConfig {
        minSdkVersion 16
        ...
        buildConfigField("String", "QA_AUTH_KEY", "\"auth_token\"")
    }
    ...
  }
 ```

 then you can access it in the code, for example to initialize the SDK.

 ```Java
 qa.init(context, BuildConfig.QA_AUTH_KEY, null);
 ```

---

## Firebase

For the best experience with the SDK we strongly recommend to add to your app [Firebase Messaging, Crashlytics and Analytics](https://firebase.google.com/), this will allow QA service to also communicate with the app to check its status and more.

---

QA Runnables
------------
In almost all the public functions of the singleton QA, you will find that they accept an object that should implements the basic QARunnable interface.
Since most of what QA does is asynchronous, this allows developers to infuse delayed behaviour when a task succeeds or when a task fails (for example if connection is not available).
The QA SDK offers an example of basic objects that implements the QA runnable interface for example the QARunnableExample and the SnackRun.

---

## Issue tracking and contact  
Feel free to use the issue tracking of this repo to report any problem with the SDK, in case of more immediate assistance need feel free to contact us at [development@quantactions.com](emailto:development@quantactions.com)
