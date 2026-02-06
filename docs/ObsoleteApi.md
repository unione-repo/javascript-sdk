# UniOne.ObsoleteApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**unsubscribedCheck**](ObsoleteApi.md#unsubscribedCheck) | **POST** /unsubscribed/check.json | Checks if an email is unsubscribed.
[**unsubscribedList**](ObsoleteApi.md#unsubscribedList) | **POST** /unsubscribed/list.json | Returns a list of all unsubscribed emails since provided date.
[**unsubscribedSet**](ObsoleteApi.md#unsubscribedSet) | **POST** /unsubscribed/set.json | Registers a new unsubscribed email.



## unsubscribedCheck

> UnsubscribedCheck200Response unsubscribedCheck(unsubscribedCheckRequest)

Checks if an email is unsubscribed.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.ObsoleteApi();

let unsubscribedCheckRequest = new UniOne.UnsubscribedCheckRequest();
unsubscribedCheckRequest.setAddress('email@example.com');

apiInstance.unsubscribedCheck(unsubscribedCheckRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **unsubscribedCheckRequest** | [**UnsubscribedCheckRequest**](UnsubscribedCheckRequest.md)|  |  |  true 

### Return type

[**UnsubscribedCheck200Response**](UnsubscribedCheck200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## unsubscribedList

> UnsubscribedList200Response unsubscribedList(unsubscribedListRequest)

Returns a list of all unsubscribed emails since provided date.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.ObsoleteApi();

let unsubscribedListRequest = new UniOne.UnsubscribedListRequest();
unsubscribedListRequest.setDateFrom('2020-10-14');

apiInstance.unsubscribedList(unsubscribedListRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **unsubscribedListRequest** | [**UnsubscribedListRequest**](UnsubscribedListRequest.md)|  |  |  true 

### Return type

[**UnsubscribedList200Response**](UnsubscribedList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## unsubscribedSet

> UnsubscribedSet200Response unsubscribedSet(unsubscribedSetRequest)

Registers a new unsubscribed email.

After registering an email as unsubscribed all future attempts to send a message to this email will be rejected. Please note that there's no way to remove an email from unsubscribed thru the API. But you can send an email with a link to resubscribe using [email/subscribe](https://docs.unione.io/en/web-api-ref#email-subscribe) method or remove **unsubscribed** status manually on [Email Search page](https://cp.unione.io/en/user/email) in control panel (but only a limited number of unsubscribed email per day can be removed).

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.ObsoleteApi();

let unsubscribedSetRequest = new UniOne.UnsubscribedSetRequest();
unsubscribedSetRequest.setAddress('email@example.com');

apiInstance.unsubscribedSet(unsubscribedSetRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **unsubscribedSetRequest** | [**UnsubscribedSetRequest**](UnsubscribedSetRequest.md)|  |  |  true 

### Return type

[**UnsubscribedSet200Response**](UnsubscribedSet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

