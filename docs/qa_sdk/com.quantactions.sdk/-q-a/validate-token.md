//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[validateToken](validate-token.md)

# validateToken

[androidJvm]\
open fun [validateToken](validate-token.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), authCode: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<Resource<[TapCloudResponse](../../com.quantactions.sdk.data.api.responses/-tap-cloud-response/index.md)>>

#### Return

LiveData object containing the status of the response and the message from the API.

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| authCode | Authentication token to be tested |
