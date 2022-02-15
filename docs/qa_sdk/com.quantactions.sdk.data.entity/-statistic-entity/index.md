//[qa_sdk](../../../index.md)/[com.quantactions.sdk.data.entity](../index.md)/[StatisticEntity](index.md)

# StatisticEntity

[androidJvm]\
@JsonClass(generateAdapter = true)

data class [StatisticEntity](index.md)(**id**: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), **stat**: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), **timestamp**: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), **value**: [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html), **timeZone**: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), **reset**: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html))

Entity of QA statistics obtained from the TapCloud API. In particular this is the entity for the numeric stats. The numeric stat is generally stored as a value corresponding to the score in the last 24 hours. Since the scores are calculated over 24 hours window the API provides scores with window strides of 1 hour, in this way no matter the Time Zone a device can retrieve the score corresponding to the correct time zone shift. To understand which subsets of the scores a device has to retrieve, one can simply extract all of the scores where the 'reset' value of the ROW is equal to the raw time shift in the current time zone.

## Constructors

| | |
|---|---|
| [StatisticEntity](-statistic-entity.md) | [androidJvm]<br>fun [StatisticEntity](-statistic-entity.md)(id: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), stat: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), timestamp: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), value: [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html), timeZone: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), reset: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)) |

## Properties

| Name | Summary |
|---|---|
| [id](id.md) | [androidJvm]<br>val [id](id.md): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Unique, defined as the concatenation between UNIX timestamp and stat code |
| [reset](reset.md) | [androidJvm]<br>val [reset](reset.md): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Value corresponding to the raw offset for which the 24-hours window was selected to calculate the stat. |
| [stat](stat.md) | [androidJvm]<br>val [stat](stat.md): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>stat code e.g. |
| [timestamp](timestamp.md) | [androidJvm]<br>val [timestamp](timestamp.md): [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)<br>UNIX timestamp in milliseconds of the entry score |
| [timeZone](time-zone.md) | [androidJvm]<br>val [timeZone](time-zone.md): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>ID of the time zone e.g. |
| [value](value.md) | [androidJvm]<br>val [value](value.md): [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)<br>Value of the score e.g. |
