# UniOne.EventDumpApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**eventDumpCreate**](EventDumpApi.md#eventDumpCreate) | **POST** /event-dump/create.json | This asynchronous method initiates the preparation of data dump in CSV format. The number of dump files created or stored is limited to 10; to order more files, you have to delete one of the previous ones or wait until they will be deleted automatically. A newly created dump file is kept for 8 hours. If the request period is more than a day or there are too many events then several files will be generated and each file will contain no more than 100,000 events. File contains columns with the following information - 'event_time', 'job_id', 'from_email', 'email', 'status', 'delivery_status', 'metadata', 'destination_response', 'user_agent', 'url', 'ip', 'tags' and 'project_id' (for accounts with projects enabled). You can change the fields and include 'subject' field using 'dump_fileds' parameter.
[**eventDumpDelete**](EventDumpApi.md#eventDumpDelete) | **POST** /event-dump/delete.json | Removes dump from queue or storage.
[**eventDumpGet**](EventDumpApi.md#eventDumpGet) | **POST** /event-dump/get.json | Returns dump properties for a given identifier
[**eventDumpList**](EventDumpApi.md#eventDumpList) | **POST** /event-dump/list.json | This method does not require any parameters; returns the full list of existing dumps.



## eventDumpCreate

> EventDumpCreate200Response eventDumpCreate(eventDumpCreateRequest)

This asynchronous method initiates the preparation of data dump in CSV format. The number of dump files created or stored is limited to 10; to order more files, you have to delete one of the previous ones or wait until they will be deleted automatically. A newly created dump file is kept for 8 hours. If the request period is more than a day or there are too many events then several files will be generated and each file will contain no more than 100,000 events. File contains columns with the following information - 'event_time', 'job_id', 'from_email', 'email', 'status', 'delivery_status', 'metadata', 'destination_response', 'user_agent', 'url', 'ip', 'tags' and 'project_id' (for accounts with projects enabled). You can change the fields and include 'subject' field using 'dump_fileds' parameter.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.EventDumpApi();

let eventDumpCreateRequest = new UniOne.EventDumpCreateRequest();
eventDumpCreateRequest.setStartTime('2022-07-20 00:00:00');
eventDumpCreateRequest.setEndTime('2022-07-21 00:00:00');
eventDumpCreateRequest.setLimit(50);
eventDumpCreateRequest.setAllProjects(null);
eventDumpCreateRequest.setFilter(new UniOne.FilterObject());
eventDumpCreateRequest.setDumpFields(["string1"]);
eventDumpCreateRequest.setAggregate('day_status');
eventDumpCreateRequest.setDelimiter(';');
eventDumpCreateRequest.setFormat('csv');

apiInstance.eventDumpCreate(eventDumpCreateRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **eventDumpCreateRequest** | [**EventDumpCreateRequest**](EventDumpCreateRequest.md)|  |  |  true 

### Return type

[**EventDumpCreate200Response**](EventDumpCreate200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## eventDumpDelete

> SuccessResponse eventDumpDelete(eventDumpDeleteRequest)

Removes dump from queue or storage.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.EventDumpApi();

let eventDumpDeleteRequest = new UniOne.EventDumpDeleteRequest();
eventDumpDeleteRequest.setDumpId('Gqfasjh34tlasd');

apiInstance.eventDumpDelete(eventDumpDeleteRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **eventDumpDeleteRequest** | [**EventDumpDeleteRequest**](EventDumpDeleteRequest.md)|  |  |  true 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## eventDumpGet

> EventDumpGet200Response eventDumpGet(eventDumpGetRequest)

Returns dump properties for a given identifier

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.EventDumpApi();

let eventDumpGetRequest = new UniOne.EventDumpGetRequest();
eventDumpGetRequest.setDumpId('Gqfasjh34tlasd');

apiInstance.eventDumpGet(eventDumpGetRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **eventDumpGetRequest** | [**EventDumpGetRequest**](EventDumpGetRequest.md)|  |  |  true 

### Return type

[**EventDumpGet200Response**](EventDumpGet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## eventDumpList

> EventDumpList200Response eventDumpList()

This method does not require any parameters; returns the full list of existing dumps.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.EventDumpApi();


apiInstance.eventDumpList().then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters

This endpoint does not need any parameter.

### Return type

[**EventDumpList200Response**](EventDumpList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

