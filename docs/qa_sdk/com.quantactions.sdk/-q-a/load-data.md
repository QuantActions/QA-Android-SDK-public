//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[loadData](load-data.md)

# loadData

[androidJvm]\
open fun <[T](load-data.md) : [QARunnable](../-q-a-runnable/index.md)?> [loadData](load-data.md)(activity: [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html), @[Nullable](https://developer.android.com/reference/kotlin/androidx/annotation/Nullable.html)()runnable: T)

Triggers sending data by email. Warning this opens also the email application.

## Parameters

androidJvm

| | |
|---|---|
| activity | Android activity |
| runnable | to handle responses [com.quantactions.sdk.QARunnable](../-q-a-runnable/index.md) |
| <T> | any class that implements [com.quantactions.sdk.QARunnable](../-q-a-runnable/index.md) |
