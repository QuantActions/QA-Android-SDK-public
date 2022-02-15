//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[getStat](get-stat.md)

# getStat

[androidJvm]\
open fun [getStat](get-stat.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), statCode: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): Flow<Resource<[List](https://developer.android.com/reference/kotlin/java/util/List.html)<[StatisticEntity](../../com.quantactions.sdk.data.entity/-statistic-entity/index.md)>>>

Get stats from TapCloud relative to the device in use. You should have received separately a list of available stats for your study. Use this function to get any stat that is numeric i.e. a score value per day/hour.

#### Return

A flow wrapping a list of [StatisticEntity](../../com.quantactions.sdk.data.entity/-statistic-entity/index.md)

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| statCode | String corresponding to the stat code |
