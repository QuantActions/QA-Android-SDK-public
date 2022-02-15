//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[init](init.md)

# init

[androidJvm]\
open fun [init](init.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), authCode: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), @[Nullable](https://developer.android.com/reference/kotlin/androidx/annotation/Nullable.html)()age: [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html), @[Nullable](https://developer.android.com/reference/kotlin/androidx/annotation/Nullable.html)()gender: [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

The first time you use the QA SDK in the code you should initialize it, this allows the SDK to create a unique identifier and be recognized by the server. Most of the functionality will not work if you have never initialized the singleton before.

#### Return

if or not it was the first time that the SDK was initialized.

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| authCode | Authorization code which is provided by QA. |
