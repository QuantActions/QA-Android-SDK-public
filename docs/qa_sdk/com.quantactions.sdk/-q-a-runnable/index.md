//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QARunnable](index.md)

# QARunnable

[androidJvm]\
abstract class [QARunnable](index.md) : [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html)

This abstract class extends Runnable. Because all of the work done by the QA API is in the background and most importantly asynchronous, it is important to offer a way for the main thread to be updated as well as offering a way to collect the result (positive or negative) of a certain call. With any QA request you can submit an instance of a class that implements this interface so that the desired action is triggered in case of success or failure of the call. In order to use this runnable you need to implement this abstract class. this runnable is used for handling asynchronous response of the server. Note that some functions in the API will return immediate values on the success or failure of the submission of the call, the result of the call can only be handled by this runnable. Take a look at [QARunnableExample](../-q-a-runnable-example/index.md) and [SnackRun](../-snack-run/index.md) for some examples of what you can achieve with this Runnable.

## See also

androidJvm

| | |
|---|---|
| [com.quantactions.sdk.QARunnableExample](../-q-a-runnable-example/index.md) |  |
| [com.quantactions.sdk.SnackRun](../-snack-run/index.md) | Created by Enea Ceolini on 23/08/17. Contact: enea.ceolini@quantactions.com |

## Constructors

| | |
|---|---|
| [QARunnable](-q-a-runnable.md) | [androidJvm]<br>fun [QARunnable](-q-a-runnable.md)() |

## Types

| Name | Summary |
|---|---|
| [Companion](-companion/index.md) | [androidJvm]<br>object [Companion](-companion/index.md) |

## Functions

| Name | Summary |
|---|---|
| [getMetadata](get-metadata.md) | [androidJvm]<br>fun [getMetadata](get-metadata.md)(): [QAJSON](../-q-a-j-s-o-n/index.md)? |
| [getResponse](get-response.md) | [androidJvm]<br>fun [getResponse](get-response.md)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Method for the user to retrieve more information about the successful of faulty call. |
| [launch](launch.md) | [androidJvm]<br>fun [launch](launch.md)() |
| [run](run.md) | [androidJvm]<br>open override fun [run](run.md)()<br>The run function has ben overridden from the Runnable class so it can run the proper sub-function depending on the result of the call. |
| [runNegative](run-negative.md) | [androidJvm]<br>abstract fun [runNegative](run-negative.md)()<br>Method defining what should be run in case of negative outcome of the call |
| [runPositive](run-positive.md) | [androidJvm]<br>abstract fun [runPositive](run-positive.md)()<br>Method defining what should be run in case of positive outcome of the call |
| [setMetadata](set-metadata.md) | [androidJvm]<br>fun [setMetadata](set-metadata.md)(metadata: [QAJSON](../-q-a-j-s-o-n/index.md)) |
| [setResponse](set-response.md) | [androidJvm]<br>fun [setResponse](set-response.md)(response: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html))<br>Method for the QA Handler to set for information about the call |
| [setStatus](set-status.md) | [androidJvm]<br>fun [setStatus](set-status.md)(status: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html))<br>Method for the QA Handler to set the positive of negative outcome of the call |

## Inheritors

| Name |
|---|
| [QARunnableExample](../-q-a-runnable-example/index.md) |
| [SnackRun](../-snack-run/index.md) |
