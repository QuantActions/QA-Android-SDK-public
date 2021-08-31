//[qa_sdk](../../../index.md)/[com.quantactions.sdk.exceptions](../index.md)/[SDKNotInitialisedException](index.md)

# SDKNotInitialisedException

[androidJvm]\
class [SDKNotInitialisedException](index.md)(**message**: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) : [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html)

Exception launched when SDK functionalities are called before the SDK was initialized.

## Constructors

| | |
|---|---|
| [SDKNotInitialisedException](-s-d-k-not-initialised-exception.md) | [androidJvm]<br>fun [SDKNotInitialisedException](-s-d-k-not-initialised-exception.md)(message: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) = "SDK Not Initialised! In order to communicate with the server call" +         "\n" +         "QA qa = QA.getInstance();\n" +         "qa.init(context, your_authorization_key, null);\n" +         "\n") |

## Functions

| Name | Summary |
|---|---|
| [addSuppressed](index.md#282858770%2FFunctions%2F203928384) | [androidJvm]<br>fun [addSuppressed](index.md#282858770%2FFunctions%2F203928384)(p0: [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) |
| [fillInStackTrace](index.md#-1102069925%2FFunctions%2F203928384) | [androidJvm]<br>open fun [fillInStackTrace](index.md#-1102069925%2FFunctions%2F203928384)(): [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |
| [getLocalizedMessage](index.md#1043865560%2FFunctions%2F203928384) | [androidJvm]<br>open fun [getLocalizedMessage](index.md#1043865560%2FFunctions%2F203928384)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [getStackTrace](index.md#2050903719%2FFunctions%2F203928384) | [androidJvm]<br>open fun [getStackTrace](index.md#2050903719%2FFunctions%2F203928384)(): [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<[StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement.html)> |
| [getSuppressed](index.md#672492560%2FFunctions%2F203928384) | [androidJvm]<br>fun [getSuppressed](index.md#672492560%2FFunctions%2F203928384)(): [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)> |
| [initCause](index.md#-418225042%2FFunctions%2F203928384) | [androidJvm]<br>open fun [initCause](index.md#-418225042%2FFunctions%2F203928384)(p0: [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)): [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |
| [printStackTrace](index.md#-1769529168%2FFunctions%2F203928384) | [androidJvm]<br>open fun [printStackTrace](index.md#-1769529168%2FFunctions%2F203928384)()<br>open fun [printStackTrace](index.md#1841853697%2FFunctions%2F203928384)(p0: [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html))<br>open fun [printStackTrace](index.md#1175535278%2FFunctions%2F203928384)(p0: [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html)) |
| [setStackTrace](index.md#2135801318%2FFunctions%2F203928384) | [androidJvm]<br>open fun [setStackTrace](index.md#2135801318%2FFunctions%2F203928384)(p0: [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<[StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement.html)>) |

## Properties

| Name | Summary |
|---|---|
| [cause](index.md#1584972056%2FProperties%2F203928384) | [androidJvm]<br>open val [cause](index.md#1584972056%2FProperties%2F203928384): [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? |
| [message](index.md#1709869626%2FProperties%2F203928384) | [androidJvm]<br>open val [message](index.md#1709869626%2FProperties%2F203928384): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? |
