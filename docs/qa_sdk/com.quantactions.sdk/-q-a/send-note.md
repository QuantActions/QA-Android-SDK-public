//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[sendNote](send-note.md)

# sendNote

[androidJvm]\
open fun [sendNote](send-note.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), text: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<Resource<[TapCloudResponse](../../com.quantactions.sdk.data.api.responses/-tap-cloud-response/index.md)>>

Sends simple text note to server.

#### Return

LiveData object containing the status of the response and the message from the API.

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| text | simple text |
