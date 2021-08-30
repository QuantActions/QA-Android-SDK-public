//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[getLastTaps](get-last-taps.md)

# getLastTaps

[androidJvm]\
open fun [getLastTaps](get-last-taps.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), flag: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), currentTime: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)): [QATaps](../-q-a-taps/index.md)

Retrieves taps in the last day, week or month depending on the provided flag.

#### Return

last taps

## See also

androidJvm

| | |
|---|---|
| [com.quantactions.sdk.QAStrings](../-q-a-strings/index.md) | Please also |
| [com.quantactions.sdk.QATaps](../-q-a-taps/index.md) | for the provided result structure. Alpha feature, try setting flag as the number of days you would like to gat back. |

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
| flag | @see com.quantactions.sdk.QAStrings (or free) |
| currentTime | System.currentTimeMillis() |
