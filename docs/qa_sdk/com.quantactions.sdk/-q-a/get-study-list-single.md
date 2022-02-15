//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[getStudyListSingle](get-study-list-single.md)

# getStudyListSingle

[androidJvm]\
open fun [getStudyListSingle](get-study-list-single.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[List](https://developer.android.com/reference/kotlin/java/util/List.html)<[StudyEntity](../../com.quantactions.sdk.data.entity/-study-entity/index.md)>>

Retrieves the list of studies the device is currently registered for.

#### Return

LiveData as SingleEvent containing the list of studies the device is subscribed to. The difference with QA.getStudyList is that this function only informs of its result once.

## See also

androidJvm

| | |
|---|---|
| [com.quantactions.sdk.data.entity.StudyEntity](../../com.quantactions.sdk.data.entity/-study-entity/index.md) |  |

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
