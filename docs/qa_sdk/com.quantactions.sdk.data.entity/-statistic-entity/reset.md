//[qa_sdk](../../../index.md)/[com.quantactions.sdk.data.entity](../index.md)/[StatisticEntity](index.md)/[reset](reset.md)

# reset

[androidJvm]\
val [reset](reset.md): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)

Value corresponding to the raw offset for which the 24-hours window was selected to calculate the stat. E.g. if reset is 2 this means that users in a time zone with raw offset to GMT is +2 should use this value to identify the correct stat of the day (corresponding to a reset in THEIR midnight).
