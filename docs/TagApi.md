# UniOne.TagApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**tagDelete**](TagApi.md#tagDelete) | **POST** /tag/delete.json | Removes tag.
[**tagList**](TagApi.md#tagList) | **POST** /tag/list.json | This method returns the full list of user-defined tags. Does not receive any parameters.



## tagDelete

> SuccessResponse tagDelete(tagDeleteRequest)

Removes tag.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.TagApi();

let tagDeleteRequest = new UniOne.TagDeleteRequest();
tagDeleteRequest.setTagId(54);

apiInstance.tagDelete(tagDeleteRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **tagDeleteRequest** | [**TagDeleteRequest**](TagDeleteRequest.md)|  |  |  true 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## tagList

> TagList200Response tagList()

This method returns the full list of user-defined tags. Does not receive any parameters.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.TagApi();


apiInstance.tagList().then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters

This endpoint does not need any parameter.

### Return type

[**TagList200Response**](TagList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

