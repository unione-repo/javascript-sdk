# UniOne.SuppressionApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**suppressionDelete**](SuppressionApi.md#suppressionDelete) | **POST** /suppression/delete.json | Deletes an email from suppression list (only records with is_deletable=true). If there are no entries of this email in the suppression list, API error 3003 is returned. If such entries exist but no one can be deleted, API error 3004 is returned. If daily limit of deletes exceeded, API error 906 is returned.
[**suppressionGet**](SuppressionApi.md#suppressionGet) | **POST** /suppression/get.json | Gets a reason and date of email suppression.
[**suppressionList**](SuppressionApi.md#suppressionList) | **POST** /suppression/list.json | Returns a suppression list since provided date.
[**suppressionSet**](SuppressionApi.md#suppressionSet) | **POST** /suppression/set.json | Adds an email address to the suppression list. You can always remove this address from the suppression list later using the [suppression/delete](https://docs.unione.io/en/web-api-ref#suppression-delete) method.



## suppressionDelete

> SuccessResponse suppressionDelete(suppressionDeleteRequest)

Deletes an email from suppression list (only records with is_deletable=true). If there are no entries of this email in the suppression list, API error 3003 is returned. If such entries exist but no one can be deleted, API error 3004 is returned. If daily limit of deletes exceeded, API error 906 is returned.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.SuppressionApi();

let suppressionDeleteRequest = new UniOne.SuppressionDeleteRequest();
suppressionDeleteRequest.setEmail('email@example.com');

apiInstance.suppressionDelete(suppressionDeleteRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **suppressionDeleteRequest** | [**SuppressionDeleteRequest**](SuppressionDeleteRequest.md)|  |  |  true 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## suppressionGet

> SuppressionGet200Response suppressionGet(suppressionGetRequest)

Gets a reason and date of email suppression.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.SuppressionApi();

let suppressionGetRequest = new UniOne.SuppressionGetRequest();
suppressionGetRequest.setEmail('email@example.com');
suppressionGetRequest.setAllProjects(null);

apiInstance.suppressionGet(suppressionGetRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **suppressionGetRequest** | [**SuppressionGetRequest**](SuppressionGetRequest.md)|  |  |  true 

### Return type

[**SuppressionGet200Response**](SuppressionGet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## suppressionList

> SuppressionList200Response suppressionList(suppressionListRequest)

Returns a suppression list since provided date.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.SuppressionApi();

let suppressionListRequest = new UniOne.SuppressionListRequest();
suppressionListRequest.setCause('unsubscribed');
suppressionListRequest.setSource('user');
suppressionListRequest.setStartTime('2020-10-14 17:00:00');
suppressionListRequest.setCursor('Ajfb6Hvdkn3hdhhvG57xbdufhG5');
suppressionListRequest.setLimit(50);

apiInstance.suppressionList(suppressionListRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **suppressionListRequest** | [**SuppressionListRequest**](SuppressionListRequest.md)|  |  |  true 

### Return type

[**SuppressionList200Response**](SuppressionList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## suppressionSet

> SuccessResponse suppressionSet(suppressionSetRequest)

Adds an email address to the suppression list. You can always remove this address from the suppression list later using the [suppression/delete](https://docs.unione.io/en/web-api-ref#suppression-delete) method.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.SuppressionApi();

let suppressionSetRequest = new UniOne.SuppressionSetRequest();
suppressionSetRequest.setEmail('email@example.com');
suppressionSetRequest.setCause('unsubscribed');
suppressionSetRequest.setCreated('2021-12-19 10:15:49');

apiInstance.suppressionSet(suppressionSetRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **suppressionSetRequest** | [**SuppressionSetRequest**](SuppressionSetRequest.md)|  |  |  true 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

