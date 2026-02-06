# UniOne.WebhookApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**webhookDelete**](WebhookApi.md#webhookDelete) | **POST** /webhook/delete.json | Deletes an event notification handler
[**webhookGet**](WebhookApi.md#webhookGet) | **POST** /webhook/get.json | Gets properties of a [webhook](https://docs.unione.io/en/web-api-ref#webhook).
[**webhookList**](WebhookApi.md#webhookList) | **POST** /webhook/list.json | List all or some [webhooks](https://docs.unione.io/en/web-api-ref#webhook) (event notification handlers) of a user or a project.
[**webhookSet**](WebhookApi.md#webhookSet) | **POST** /webhook/set.json | Sets or edits a [webhook](https://docs.unione.io/en/web-api-ref#webhook), i.e. an event notification handler.



## webhookDelete

> SuccessResponse webhookDelete(webhookGetRequest)

Deletes an event notification handler

You can also temporarily deactivate webhook without deleting it by setting it's status to **disabled** in [webhook/set](https://docs.unione.io/en/web-api-ref#webhook-set) method.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.WebhookApi();

let webhookGetRequest = new UniOne.WebhookGetRequest();
webhookGetRequest.setUrl('https://example.com/webhook');

apiInstance.webhookDelete(webhookGetRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **webhookGetRequest** | [**WebhookGetRequest**](WebhookGetRequest.md)|  |  |  true 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## webhookGet

> WebhookSet200Response webhookGet(webhookGetRequest)

Gets properties of a [webhook](https://docs.unione.io/en/web-api-ref#webhook).

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.WebhookApi();

let webhookGetRequest = new UniOne.WebhookGetRequest();
webhookGetRequest.setUrl('https://example.com/webhook');

apiInstance.webhookGet(webhookGetRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **webhookGetRequest** | [**WebhookGetRequest**](WebhookGetRequest.md)|  |  |  true 

### Return type

[**WebhookSet200Response**](WebhookSet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## webhookList

> WebhookList200Response webhookList(webhookListRequest)

List all or some [webhooks](https://docs.unione.io/en/web-api-ref#webhook) (event notification handlers) of a user or a project.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.WebhookApi();

let webhookListRequest = new UniOne.WebhookListRequest();
webhookListRequest.setLimit(null);
webhookListRequest.setOffset(null);

apiInstance.webhookList(webhookListRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **webhookListRequest** | [**WebhookListRequest**](WebhookListRequest.md)|  |  |  true 

### Return type

[**WebhookList200Response**](WebhookList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## webhookSet

> WebhookSet200Response webhookSet(webhookSetRequest)

Sets or edits a [webhook](https://docs.unione.io/en/web-api-ref#webhook), i.e. an event notification handler.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.WebhookApi();

let webhookSetRequest = new UniOne.WebhookSetRequest();
webhookSetRequest.setUrl('https://yourhost.example.com/unione-webhook');
webhookSetRequest.setStatus(null);
webhookSetRequest.setEventFormat(null);
webhookSetRequest.setDeliveryInfo(null);
webhookSetRequest.setSingleEvent(null);
webhookSetRequest.setMaxParallel(null);
webhookSetRequest.setEvents(new UniOne.WebhookEventsObject());

apiInstance.webhookSet(webhookSetRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **webhookSetRequest** | [**WebhookSetRequest**](WebhookSetRequest.md)|  |  |  true 

### Return type

[**WebhookSet200Response**](WebhookSet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

