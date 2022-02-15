//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[getQuestionnairesList](get-questionnaires-list.md)

# getQuestionnairesList

[androidJvm]\
open fun [getQuestionnairesList](get-questionnaires-list.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[List](https://developer.android.com/reference/kotlin/java/util/List.html)<[QuestionnaireEntity](../../com.quantactions.sdk.data.entity/-questionnaire-entity/index.md)>>

Get a list of all the questionnaires available to complete (across all the studies to which a device is subscribed to).

#### Return

LiveData containing a list of [QuestionnaireEntity](../../com.quantactions.sdk.data.entity/-questionnaire-entity/index.md)

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
