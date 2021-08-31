//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[getLastTaps](get-last-taps.md)

# getLastTaps

[androidJvm]\
open fun [getLastTaps](get-last-taps.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), flag: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), currentTime: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)): [QATaps](../-q-a-taps/index.md)

Retrieves taps in the last day, week or month depending on the provided flag. Please also [QATaps](../-q-a-taps/index.md) shows the provided result structure. Alpha feature, try setting flag as the number of days you would like to gat back.

#### Return

last taps

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| flag | from [QA.Flags](-flags/index.md) |
| currentTime | System.currentTimeMillis() |
