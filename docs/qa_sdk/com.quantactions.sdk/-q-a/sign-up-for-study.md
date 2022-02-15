//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[signUpForStudy](sign-up-for-study.md)

# signUpForStudy

[androidJvm]\
open fun [signUpForStudy](sign-up-for-study.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), participationId: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<Resource<StudyWithQuestionnaires>>

Use this function to subscribe the device to a certain study. The runnable

#### Return

LiveData object containing the status of the response and the StudyWithQuestionnaires object. The Resource will hold info about the study if the call is successfull or a message about the failed call.

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| participationId | to the study, or the studyId if it's a generic subscription. |
