//[qa_sdk](../../index.md)/[com.quantactions.sdk](index.md)

# Package com.quantactions.sdk

## Types

| Name | Summary |
|---|---|
| [DatabaseHelper](-database-helper/index.md) | [androidJvm]<br>open class [DatabaseHelper](-database-helper/index.md) : [SQLiteOpenHelper](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOpenHelper.html) |
| [FileHolder](-file-holder/index.md) | [androidJvm]<br>open class [FileHolder](-file-holder/index.md)<br>FileHolder is a class that gives easy access to every file saved in the app context. |
| [LookUp](-look-up/index.md) | [androidJvm]<br>interface [LookUp](-look-up/index.md)<br>Created By Enea Ceolini 2015 Contact: enea.ceolini@quantactions. |
| [ManagePref2](-manage-pref2/index.md) | [androidJvm]<br>class [ManagePref2](-manage-pref2/index.md) |
| [QA](-q-a/index.md) | [androidJvm]<br>open class [QA](-q-a/index.md)<br>This is the main element one needs to use to access all the functionality of the QA SDK. |
| [QABroadcastReceiver](-q-a-broadcast-receiver/index.md) | [androidJvm]<br>open class [QABroadcastReceiver](-q-a-broadcast-receiver/index.md) : [BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html)<br>General broadcast receiver for SDK actions. |
| [QAFirebaseMessagingService](-q-a-firebase-messaging-service/index.md) | [androidJvm]<br>open class [QAFirebaseMessagingService](-q-a-firebase-messaging-service/index.md) : FirebaseMessagingService<br>This basic service handles Firebase messaging, thus it handles what happens when a notification is received from the cloud (from tap admin). |
| [QAStrings](-q-a-strings/index.md) | [androidJvm]<br>interface [QAStrings](-q-a-strings/index.md)<br>Various codes for QA SDK. |
| [QATaps](-q-a-taps/index.md) | [androidJvm]<br>class [QATaps](-q-a-taps/index.md)(**taps**: [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?, **total_taps**: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), **speed**: [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?)<br>This class will contain the result to the call {@link com.quantactions.sdk.QA.getLastTaps} The length of taps and speed depends on the number of days requested. |
| [ReadingsService](-readings-service/index.md) | [androidJvm]<br>open class [ReadingsService](-readings-service/index.md) : [Service](https://developer.android.com/reference/kotlin/android/app/Service.html)<br>Background service (forced to be foreground for SDK >= Android O) that allows QA to function properly. |
| [RelaunchWorker](-relaunch-worker/index.md) | [androidJvm]<br>open class [RelaunchWorker](-relaunch-worker/index.md) : [Worker](https://developer.android.com/reference/kotlin/androidx/work/Worker.html) |
| [ServiceStarter](-service-starter/index.md) | [androidJvm]<br>open class [ServiceStarter](-service-starter/index.md) : [Worker](https://developer.android.com/reference/kotlin/androidx/work/Worker.html) |
| [SingletonHolder](-singleton-holder/index.md) | [androidJvm]<br>open class [SingletonHolder](-singleton-holder/index.md)<out [T](-singleton-holder/index.md), in [A](-singleton-holder/index.md)>(**creator**: ([A](-singleton-holder/index.md)) -> [T](-singleton-holder/index.md)) |
| [SyncWorker](-sync-worker/index.md) | [androidJvm]<br>open class [SyncWorker](-sync-worker/index.md) : [Worker](https://developer.android.com/reference/kotlin/androidx/work/Worker.html) |
