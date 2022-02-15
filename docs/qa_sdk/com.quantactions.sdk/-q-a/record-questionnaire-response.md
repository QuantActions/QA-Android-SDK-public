//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[recordQuestionnaireResponse](record-questionnaire-response.md)

# recordQuestionnaireResponse

[androidJvm]\
open fun [recordQuestionnaireResponse](record-questionnaire-response.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), name: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), code: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), date: [Long](https://developer.android.com/reference/kotlin/java/lang/Long.html), fullID: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), response: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<Resource<[TapCloudResponse](../../com.quantactions.sdk.data.api.responses/-tap-cloud-response/index.md)>>

#### Return

LiveData object containing the status of the response and the message from the API.

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| name | Name of the questionnaire (one gets this from the Questionnaire Entity) |
| code | Code of the questionnaire (one gets this from the Questionnaire Entity) |
| date | UNIX Timestamp in milliseconds of the time of completion (e.g. System.currentTimeMillis()) |
| fullID | Full ID id of the questionnaire = study_id+questionnaire_code |
| response | JSON encoded string with the response to the questionnaire, i.e. key-value map where key == question key , value == numeric answer |
