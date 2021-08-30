//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[signUpForStudy](sign-up-for-study.md)

# signUpForStudy

[androidJvm]\
open fun <[T](sign-up-for-study.md) : [QARunnable](../-q-a-runnable/index.md)?> [signUpForStudy](sign-up-for-study.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), participationId: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), runnable: T)

Use this function to subscribe the device to a certain study. The runnable metadata is filled with a [com.quantactions.sdk.QAJSON](../-q-a-j-s-o-n/index.md) with the following fields: 

COLUMN_STUDY_ID

COLUMN_STUDY_TITLE

COLUMN_WITHDRAW

COLUMN_PRIVACY

COLUMN_SYNC_SCREEN_OFF

COLUMN_PERM_APP_ID

COLUMN_PERM_DRAW

COLUMN_PERM_LOC

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| participationId | to the study |
| runnable | to handle responses [com.quantactions.sdk.QARunnable](../-q-a-runnable/index.md) |
| <T> | any class that implements [com.quantactions.sdk.QARunnable](../-q-a-runnable/index.md) |
