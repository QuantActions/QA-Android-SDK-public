//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[RelaunchWorker](index.md)

# RelaunchWorker

[androidJvm]\
open class [RelaunchWorker](index.md) : [Worker](https://developer.android.com/reference/kotlin/androidx/work/Worker.html)

## Constructors

| | |
|---|---|
| [RelaunchWorker](-relaunch-worker.md) | [androidJvm]<br>open fun [RelaunchWorker](-relaunch-worker.md)(@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)()context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html), @[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)()params: [WorkerParameters](https://developer.android.com/reference/kotlin/androidx/work/WorkerParameters.html)) |

## Functions

| Name | Summary |
|---|---|
| [doWork](do-work.md) | [androidJvm]<br>@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)()<br>open fun [doWork](do-work.md)(): [ListenableWorker.Result](https://developer.android.com/reference/kotlin/androidx/work/ListenableWorker.Result.html) |
| [getApplicationContext](../-service-starter/index.md#-560782721%2FFunctions%2F203928384) | [androidJvm]<br>fun [getApplicationContext](../-service-starter/index.md#-560782721%2FFunctions%2F203928384)(): [Context](https://developer.android.com/reference/kotlin/android/content/Context.html) |
| [getApplicationName](get-application-name.md) | [androidJvm]<br>open fun [getApplicationName](get-application-name.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)): [String](https://developer.android.com/reference/kotlin/java/lang/String.html) |
| [getBackgroundExecutor](../-service-starter/index.md#1421258461%2FFunctions%2F203928384) | [androidJvm]<br>open fun [getBackgroundExecutor](../-service-starter/index.md#1421258461%2FFunctions%2F203928384)(): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html) |
| [getForegroundInfoAsync](../-service-starter/index.md#-33123919%2FFunctions%2F203928384) | [androidJvm]<br>open fun [getForegroundInfoAsync](../-service-starter/index.md#-33123919%2FFunctions%2F203928384)(): ListenableFuture<[ForegroundInfo](https://developer.android.com/reference/kotlin/androidx/work/ForegroundInfo.html)> |
| [getId](../-service-starter/index.md#-1759193821%2FFunctions%2F203928384) | [androidJvm]<br>fun [getId](../-service-starter/index.md#-1759193821%2FFunctions%2F203928384)(): [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html) |
| [getInputData](../-service-starter/index.md#-907781528%2FFunctions%2F203928384) | [androidJvm]<br>fun [getInputData](../-service-starter/index.md#-907781528%2FFunctions%2F203928384)(): [Data](https://developer.android.com/reference/kotlin/androidx/work/Data.html) |
| [getNetwork](../-service-starter/index.md#-1225012274%2FFunctions%2F203928384) | [androidJvm]<br>fun [getNetwork](../-service-starter/index.md#-1225012274%2FFunctions%2F203928384)(): [Network](https://developer.android.com/reference/kotlin/android/net/Network.html) |
| [getRunAttemptCount](../-service-starter/index.md#1096617839%2FFunctions%2F203928384) | [androidJvm]<br>fun [getRunAttemptCount](../-service-starter/index.md#1096617839%2FFunctions%2F203928384)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [getTags](../-service-starter/index.md#1356325797%2FFunctions%2F203928384) | [androidJvm]<br>fun [getTags](../-service-starter/index.md#1356325797%2FFunctions%2F203928384)(): [Set](https://developer.android.com/reference/kotlin/java/util/Set.html)<[String](https://developer.android.com/reference/kotlin/java/lang/String.html)> |
| [getTaskExecutor](../-service-starter/index.md#1625383462%2FFunctions%2F203928384) | [androidJvm]<br>open fun [getTaskExecutor](../-service-starter/index.md#1625383462%2FFunctions%2F203928384)(): TaskExecutor |
| [getTriggeredContentAuthorities](../-service-starter/index.md#514689021%2FFunctions%2F203928384) | [androidJvm]<br>fun [getTriggeredContentAuthorities](../-service-starter/index.md#514689021%2FFunctions%2F203928384)(): [List](https://developer.android.com/reference/kotlin/java/util/List.html)<[String](https://developer.android.com/reference/kotlin/java/lang/String.html)> |
| [getTriggeredContentUris](../-service-starter/index.md#-1016068107%2FFunctions%2F203928384) | [androidJvm]<br>fun [getTriggeredContentUris](../-service-starter/index.md#-1016068107%2FFunctions%2F203928384)(): [List](https://developer.android.com/reference/kotlin/java/util/List.html)<[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html)> |
| [getWorkerFactory](../-service-starter/index.md#-473896752%2FFunctions%2F203928384) | [androidJvm]<br>open fun [getWorkerFactory](../-service-starter/index.md#-473896752%2FFunctions%2F203928384)(): [WorkerFactory](https://developer.android.com/reference/kotlin/androidx/work/WorkerFactory.html) |
| [isRunInForeground](../-service-starter/index.md#-1414702901%2FFunctions%2F203928384) | [androidJvm]<br>open fun [isRunInForeground](../-service-starter/index.md#-1414702901%2FFunctions%2F203928384)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isStopped](../-service-starter/index.md#-43937871%2FFunctions%2F203928384) | [androidJvm]<br>fun [isStopped](../-service-starter/index.md#-43937871%2FFunctions%2F203928384)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [isUsed](../-service-starter/index.md#2101847327%2FFunctions%2F203928384) | [androidJvm]<br>fun [isUsed](../-service-starter/index.md#2101847327%2FFunctions%2F203928384)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [onStopped](../-service-starter/index.md#-152470426%2FFunctions%2F203928384) | [androidJvm]<br>open fun [onStopped](../-service-starter/index.md#-152470426%2FFunctions%2F203928384)() |
| [setForegroundAsync](../-service-starter/index.md#-1269350234%2FFunctions%2F203928384) | [androidJvm]<br>fun [setForegroundAsync](../-service-starter/index.md#-1269350234%2FFunctions%2F203928384)(foregroundInfo: [ForegroundInfo](https://developer.android.com/reference/kotlin/androidx/work/ForegroundInfo.html)): ListenableFuture<[Void](https://developer.android.com/reference/kotlin/java/lang/Void.html)> |
| [setProgressAsync](../-service-starter/index.md#-348364649%2FFunctions%2F203928384) | [androidJvm]<br>open fun [setProgressAsync](../-service-starter/index.md#-348364649%2FFunctions%2F203928384)(data: [Data](https://developer.android.com/reference/kotlin/androidx/work/Data.html)): ListenableFuture<[Void](https://developer.android.com/reference/kotlin/java/lang/Void.html)> |
| [setRunInForeground](../-service-starter/index.md#1618392389%2FFunctions%2F203928384) | [androidJvm]<br>open fun [setRunInForeground](../-service-starter/index.md#1618392389%2FFunctions%2F203928384)(runInForeground: [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)) |
| [setUsed](../-service-starter/index.md#1019169525%2FFunctions%2F203928384) | [androidJvm]<br>fun [setUsed](../-service-starter/index.md#1019169525%2FFunctions%2F203928384)() |
| [startWork](../-service-starter/index.md#495345602%2FFunctions%2F203928384) | [androidJvm]<br>fun [startWork](../-service-starter/index.md#495345602%2FFunctions%2F203928384)(): ListenableFuture<[ListenableWorker.Result](https://developer.android.com/reference/kotlin/androidx/work/ListenableWorker.Result.html)> |
| [stop](../-service-starter/index.md#-441314364%2FFunctions%2F203928384) | [androidJvm]<br>fun [stop](../-service-starter/index.md#-441314364%2FFunctions%2F203928384)() |
