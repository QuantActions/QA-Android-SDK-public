//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[ServiceStarter](index.md)

# ServiceStarter

[androidJvm]\
open class [ServiceStarter](index.md) : [Worker](https://developer.android.com/reference/kotlin/androidx/work/Worker.html)

## Constructors

| | |
|---|---|
| [ServiceStarter](-service-starter.md) | [androidJvm]<br>open fun [ServiceStarter](-service-starter.md)(@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)()context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), @[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)()params: [WorkerParameters](https://developer.android.com/reference/kotlin/androidx/work/WorkerParameters.html)) |

## Functions

| Name | Summary |
|---|---|
| [doWork](do-work.md) | [androidJvm]<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)()<br>open fun [doWork](do-work.md)(): [ListenableWorker.Result](https://developer.android.com/reference/kotlin/androidx/work/ListenableWorker.Result.html) |
| [getApplicationContext](index.md#-560782721%2FFunctions%2F203928384) | [androidJvm]<br>fun [getApplicationContext](index.md#-560782721%2FFunctions%2F203928384)(): [Context](https://developer.android.com/reference/kotlin/android/content/Context.html) |
| [getBackgroundExecutor](index.md#1421258461%2FFunctions%2F203928384) | [androidJvm]<br>open fun [getBackgroundExecutor](index.md#1421258461%2FFunctions%2F203928384)(): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html) |
| [getForegroundInfoAsync](index.md#-33123919%2FFunctions%2F203928384) | [androidJvm]<br>open fun [getForegroundInfoAsync](index.md#-33123919%2FFunctions%2F203928384)(): ListenableFuture<[ForegroundInfo](https://developer.android.com/reference/kotlin/androidx/work/ForegroundInfo.html)> |
| [getId](index.md#-1759193821%2FFunctions%2F203928384) | [androidJvm]<br>fun [getId](index.md#-1759193821%2FFunctions%2F203928384)(): [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html) |
| [getInputData](index.md#-907781528%2FFunctions%2F203928384) | [androidJvm]<br>fun [getInputData](index.md#-907781528%2FFunctions%2F203928384)(): [Data](https://developer.android.com/reference/kotlin/androidx/work/Data.html) |
| [getNetwork](index.md#-1225012274%2FFunctions%2F203928384) | [androidJvm]<br>fun [getNetwork](index.md#-1225012274%2FFunctions%2F203928384)(): [Network](https://developer.android.com/reference/kotlin/android/net/Network.html) |
| [getRunAttemptCount](index.md#1096617839%2FFunctions%2F203928384) | [androidJvm]<br>fun [getRunAttemptCount](index.md#1096617839%2FFunctions%2F203928384)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [getTags](index.md#1356325797%2FFunctions%2F203928384) | [androidJvm]<br>fun [getTags](index.md#1356325797%2FFunctions%2F203928384)(): [Set](https://developer.android.com/reference/kotlin/java/util/Set.html)<[String](https://developer.android.com/reference/kotlin/java/lang/String.html)> |
| [getTaskExecutor](index.md#1625383462%2FFunctions%2F203928384) | [androidJvm]<br>open fun [getTaskExecutor](index.md#1625383462%2FFunctions%2F203928384)(): TaskExecutor |
| [getTriggeredContentAuthorities](index.md#514689021%2FFunctions%2F203928384) | [androidJvm]<br>fun [getTriggeredContentAuthorities](index.md#514689021%2FFunctions%2F203928384)(): [List](https://developer.android.com/reference/kotlin/java/util/List.html)<[String](https://developer.android.com/reference/kotlin/java/lang/String.html)> |
| [getTriggeredContentUris](index.md#-1016068107%2FFunctions%2F203928384) | [androidJvm]<br>fun [getTriggeredContentUris](index.md#-1016068107%2FFunctions%2F203928384)(): [List](https://developer.android.com/reference/kotlin/java/util/List.html)<[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html)> |
| [getWorkerFactory](index.md#-473896752%2FFunctions%2F203928384) | [androidJvm]<br>open fun [getWorkerFactory](index.md#-473896752%2FFunctions%2F203928384)(): [WorkerFactory](https://developer.android.com/reference/kotlin/androidx/work/WorkerFactory.html) |
| [isRunInForeground](index.md#-1414702901%2FFunctions%2F203928384) | [androidJvm]<br>open fun [isRunInForeground](index.md#-1414702901%2FFunctions%2F203928384)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isStopped](index.md#-43937871%2FFunctions%2F203928384) | [androidJvm]<br>fun [isStopped](index.md#-43937871%2FFunctions%2F203928384)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isUsed](index.md#2101847327%2FFunctions%2F203928384) | [androidJvm]<br>fun [isUsed](index.md#2101847327%2FFunctions%2F203928384)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [onStopped](index.md#-152470426%2FFunctions%2F203928384) | [androidJvm]<br>open fun [onStopped](index.md#-152470426%2FFunctions%2F203928384)() |
| [setForegroundAsync](index.md#-1269350234%2FFunctions%2F203928384) | [androidJvm]<br>fun [setForegroundAsync](index.md#-1269350234%2FFunctions%2F203928384)(foregroundInfo: [ForegroundInfo](https://developer.android.com/reference/kotlin/androidx/work/ForegroundInfo.html)): ListenableFuture<[Void](https://developer.android.com/reference/kotlin/java/lang/Void.html)> |
| [setProgressAsync](index.md#-348364649%2FFunctions%2F203928384) | [androidJvm]<br>open fun [setProgressAsync](index.md#-348364649%2FFunctions%2F203928384)(data: [Data](https://developer.android.com/reference/kotlin/androidx/work/Data.html)): ListenableFuture<[Void](https://developer.android.com/reference/kotlin/java/lang/Void.html)> |
| [setRunInForeground](index.md#1618392389%2FFunctions%2F203928384) | [androidJvm]<br>open fun [setRunInForeground](index.md#1618392389%2FFunctions%2F203928384)(runInForeground: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)) |
| [setUsed](index.md#1019169525%2FFunctions%2F203928384) | [androidJvm]<br>fun [setUsed](index.md#1019169525%2FFunctions%2F203928384)() |
| [startWork](index.md#495345602%2FFunctions%2F203928384) | [androidJvm]<br>fun [startWork](index.md#495345602%2FFunctions%2F203928384)(): ListenableFuture<[ListenableWorker.Result](https://developer.android.com/reference/kotlin/androidx/work/ListenableWorker.Result.html)> |
| [stop](index.md#-441314364%2FFunctions%2F203928384) | [androidJvm]<br>fun [stop](index.md#-441314364%2FFunctions%2F203928384)() |
