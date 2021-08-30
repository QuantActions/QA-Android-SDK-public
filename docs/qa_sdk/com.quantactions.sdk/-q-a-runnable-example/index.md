//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QARunnableExample](index.md)

# QARunnableExample

[androidJvm]\
class [QARunnableExample](index.md)(**context**: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), **alertDialog**: [AlertDialog](https://developer.android.com/reference/kotlin/androidx/appcompat/app/AlertDialog.html)?) : [QARunnable](../-q-a-runnable/index.md)

Implementation example of abstract interface

## See also

androidJvm

| | |
|---|---|
| [com.quantactions.sdk.QARunnable](../-q-a-runnable/index.md) | This QARunnable example shows how to add an alert dialog to the runnable, in this way the user can be notified that the app is performing a task in the background, when done the dialog is dismissed and a message appears in the SnackBar. Created by Enea Ceolini on 23/08/17. Contact: enea.ceolini@quantactions.com |

## Constructors

| | |
|---|---|
| [QARunnableExample](-q-a-runnable-example.md) | [androidJvm]<br>fun [QARunnableExample](-q-a-runnable-example.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), alertDialog: [AlertDialog](https://developer.android.com/reference/kotlin/androidx/appcompat/app/AlertDialog.html)?) |

## Functions

| Name | Summary |
|---|---|
| [getMetadata](../-q-a-runnable/get-metadata.md) | [androidJvm]<br>fun [getMetadata](../-q-a-runnable/get-metadata.md)(): [QAJSON](../-q-a-j-s-o-n/index.md)? |
| [getResponse](../-q-a-runnable/get-response.md) | [androidJvm]<br>fun [getResponse](../-q-a-runnable/get-response.md)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Method for the user to retrieve more information about the successful of faulty call. |
| [launch](../-q-a-runnable/launch.md) | [androidJvm]<br>fun [launch](../-q-a-runnable/launch.md)() |
| [run](../-q-a-runnable/run.md) | [androidJvm]<br>open override fun [run](../-q-a-runnable/run.md)()<br>The run function has ben overridden from the Runnable class so it can run the proper sub-function depending on the result of the call. |
| [runNegative](run-negative.md) | [androidJvm]<br>open override fun [runNegative](run-negative.md)()<br>Method defining what should be run in case of negative outcome of the call |
| [runPositive](run-positive.md) | [androidJvm]<br>open override fun [runPositive](run-positive.md)()<br>Method defining what should be run in case of positive outcome of the call |
| [setMetadata](../-q-a-runnable/set-metadata.md) | [androidJvm]<br>fun [setMetadata](../-q-a-runnable/set-metadata.md)(metadata: [QAJSON](../-q-a-j-s-o-n/index.md)) |
| [setResponse](../-q-a-runnable/set-response.md) | [androidJvm]<br>fun [setResponse](../-q-a-runnable/set-response.md)(response: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html))<br>Method for the QA Handler to set for information about the call |
| [setStatus](../-q-a-runnable/set-status.md) | [androidJvm]<br>fun [setStatus](../-q-a-runnable/set-status.md)(status: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html))<br>Method for the QA Handler to set the positive of negative outcome of the call |
