# UniOne.EventDumpObject

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**dumpId** | **String** | Dump ID received by the method [event-dump/create](https://docs.unione.io/en/web-api-ref#event-dump-create). |  |  true 
**dumpStatus** | **String** | Task status, possible values are:<br><br>* __queued__ - the task is in the queue, processing is not started yet;* __in_process__ - the request is being processed;* __ready__ - the task is finished, dump file is ready for download;* __failed__ - processing failed due to an internal error. |  |  true 
**files** | [**[EventDumpFilesObject]**](EventDumpFilesObject.md) | An array of objects, each representing a file, ready for download. You may start downloading everything listed in “files” even if **dump_status** is still **in_process**. If there are no events, according to the specified parameters, an empty array will be returned. |  | 


