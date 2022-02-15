//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[getBasicInfo](get-basic-info.md)

# getBasicInfo

[androidJvm]\
open fun [getBasicInfo](get-basic-info.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)): [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html)<[String](https://developer.android.com/reference/kotlin/java/lang/String.html), [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)>

#### Return

a map of information, for now only "age" (year) and "gender" (0, 1, -1)

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context. |

#### Throws

| | |
|---|---|
| [com.quantactions.sdk.exceptions.SDKNotInitialisedException](../../com.quantactions.sdk.exceptions/-s-d-k-not-initialised-exception/index.md) | if the SDK was not initialized |
