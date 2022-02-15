//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[QA](index.md)/[syncData](sync-data.md)

# syncData

[androidJvm]\
open fun [syncData](sync-data.md)(context: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html)): [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html)

Utility function to sync all the local data with the server. IDUe to the complexity of the work, it spawns Worker and return its UUID. The status of the worker can be observed to check its status of SUCCESS/FAILURE.

## Parameters

androidJvm

| | |
|---|---|
| context | Android application context |
