//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[getStatString](get-stat-string.md)

# getStatString

[androidJvm]\
open fun [getStatString](get-stat-string.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), statCode: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): Flow<Resource<[List](https://developer.android.com/reference/kotlin/java/util/List.html)<[StatisticStringEntity](../../com.quantactions.sdk.data.entity/-statistic-string-entity/index.md)>>>

Get string stats from TapCloud relative to the device in use. You should have received separately a list of available stats for your study. Use this function to get any stat that is string-encoded that is a value that includes hours:minutes of usage (e.g. 03:45).

#### Return

A flow wrapping a list of [StatisticEntity](../../com.quantactions.sdk.data.entity/-statistic-entity/index.md)

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| statCode | String corresponding to the stat code |
