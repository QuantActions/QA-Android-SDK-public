//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[signUpForStudy](sign-up-for-study.md)

# signUpForStudy

[androidJvm]\
open fun <[T](sign-up-for-study.md) : [QARunnable](../-q-a-runnable/index.md)?> [signUpForStudy](sign-up-for-study.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), participationId: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), runnable: T)

Use this function to subscribe the device to a certain study. The runnable metadata is filled with a [QAJSON](../-q-a-j-s-o-n/index.md) with the following fields: 

[STUDY_ID](-metadata/-s-t-u-d-y_-i-d.md)

[STUDY_TITLE](-metadata/-s-t-u-d-y_-t-i-t-l-e.md)

[CAN_WITHDRAW](-metadata/-c-a-n_-w-i-t-h-d-r-a-w.md)

[PRIVACY_POLICY](-metadata/-p-r-i-v-a-c-y_-p-o-l-i-c-y.md)

[PERM_APP_ID](-metadata/-p-e-r-m_-a-p-p_-i-d.md)

[PERM_DRAW](-metadata/-p-e-r-m_-d-r-a-w.md)

[PERM_LOC](-metadata/-p-e-r-m_-l-o-c.md)

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| participationId | to the study, or the studyId if it's a generic subscription. |
| runnable | to handle responses [QARunnable](../-q-a-runnable/index.md) |
| <T> | any class that implements [QARunnable](../-q-a-runnable/index.md) |
