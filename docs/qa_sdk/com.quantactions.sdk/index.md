//[qa_sdk](../../index.md)/[com.quantactions.sdk](index.md)

# Package com.quantactions.sdk

## Types

| Name | Summary |
|---|---|
| [QA](-q-a/index.md) | [androidJvm]<br>open class [QA](-q-a/index.md)<br>This is the main element one needs to use to access all the functionality of the QA SDK. |
| [QAFirebaseMessagingService](-q-a-firebase-messaging-service/index.md) | [androidJvm]<br>open class [QAFirebaseMessagingService](-q-a-firebase-messaging-service/index.md) : FirebaseMessagingService<br>This basic service handles Firebase messaging, thus it handles what happens when a notification is received from the cloud (from tap admin). |
| [QAStrings](-q-a-strings/index.md) | [androidJvm]<br>interface [QAStrings](-q-a-strings/index.md)<br>Various codes for QA SDK. |
| [QATaps](-q-a-taps/index.md) | [androidJvm]<br>class [QATaps](-q-a-taps/index.md)(**taps**: [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?, **total_taps**: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), **speed**: [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?)<br>This class will contain the result to the call {@link com.quantactions.sdk.QA.getLastTaps} The length of taps and speed depends on the number of days requested. |
