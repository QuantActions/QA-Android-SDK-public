//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QABroadcastReceiver](index.md)

# QABroadcastReceiver

[androidJvm]\
open class [QABroadcastReceiver](index.md) : [BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html)

Created by enea on 13/08/17. Contact: enea.ceolini@gmail.com

## Functions

| Name | Summary |
|---|---|
| [abortBroadcast](index.md#-1578158536%2FFunctions%2F203928384) | [androidJvm]<br>fun [abortBroadcast](index.md#-1578158536%2FFunctions%2F203928384)() |
| [clearAbortBroadcast](index.md#-547655405%2FFunctions%2F203928384) | [androidJvm]<br>fun [clearAbortBroadcast](index.md#-547655405%2FFunctions%2F203928384)() |
| [getAbortBroadcast](index.md#1852574954%2FFunctions%2F203928384) | [androidJvm]<br>fun [getAbortBroadcast](index.md#1852574954%2FFunctions%2F203928384)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [getBatteryPercentage](get-battery-percentage.md) | [androidJvm]<br>open fun [getBatteryPercentage](get-battery-percentage.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [getDebugUnregister](index.md#-2066178064%2FFunctions%2F203928384) | [androidJvm]<br>fun [getDebugUnregister](index.md#-2066178064%2FFunctions%2F203928384)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [getResultCode](index.md#-1855658543%2FFunctions%2F203928384) | [androidJvm]<br>fun [getResultCode](index.md#-1855658543%2FFunctions%2F203928384)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [getResultData](index.md#485630644%2FFunctions%2F203928384) | [androidJvm]<br>fun [getResultData](index.md#485630644%2FFunctions%2F203928384)(): [String](https://developer.android.com/reference/kotlin/java/lang/String.html) |
| [getResultExtras](index.md#153681375%2FFunctions%2F203928384) | [androidJvm]<br>fun [getResultExtras](index.md#153681375%2FFunctions%2F203928384)(makeMap: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html) |
| [goAsync](index.md#478464125%2FFunctions%2F203928384) | [androidJvm]<br>fun [goAsync](index.md#478464125%2FFunctions%2F203928384)(): [BroadcastReceiver.PendingResult](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.PendingResult.html) |
| [isInitialStickyBroadcast](index.md#-448034677%2FFunctions%2F203928384) | [androidJvm]<br>fun [isInitialStickyBroadcast](index.md#-448034677%2FFunctions%2F203928384)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isOrderedBroadcast](index.md#1250697259%2FFunctions%2F203928384) | [androidJvm]<br>fun [isOrderedBroadcast](index.md#1250697259%2FFunctions%2F203928384)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [onReceive](on-receive.md) | [androidJvm]<br>open fun [onReceive](on-receive.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), intent: [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html)) |
| [peekService](index.md#-1162131393%2FFunctions%2F203928384) | [androidJvm]<br>open fun [peekService](index.md#-1162131393%2FFunctions%2F203928384)(myContext: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), service: [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html)): [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html) |
| [setAlarm](set-alarm.md) | [androidJvm]<br>open fun [setAlarm](set-alarm.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)) |
| [setDebugUnregister](index.md#-1900628066%2FFunctions%2F203928384) | [androidJvm]<br>fun [setDebugUnregister](index.md#-1900628066%2FFunctions%2F203928384)(debug: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)) |
| [setOrderedHint](index.md#-1505624509%2FFunctions%2F203928384) | [androidJvm]<br>fun [setOrderedHint](index.md#-1505624509%2FFunctions%2F203928384)(isOrdered: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)) |
| [setResult](index.md#1636890479%2FFunctions%2F203928384) | [androidJvm]<br>fun [setResult](index.md#1636890479%2FFunctions%2F203928384)(code: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), data: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), extras: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)) |
| [setResultCode](index.md#-1280302706%2FFunctions%2F203928384) | [androidJvm]<br>fun [setResultCode](index.md#-1280302706%2FFunctions%2F203928384)(code: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)) |
| [setResultData](index.md#-2037197789%2FFunctions%2F203928384) | [androidJvm]<br>fun [setResultData](index.md#-2037197789%2FFunctions%2F203928384)(data: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)) |
| [setResultExtras](index.md#1065610694%2FFunctions%2F203928384) | [androidJvm]<br>fun [setResultExtras](index.md#1065610694%2FFunctions%2F203928384)(extras: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)) |
