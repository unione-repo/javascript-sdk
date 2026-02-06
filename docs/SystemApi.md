# UniOne.SystemApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**systemInfo**](SystemApi.md#systemInfo) | **POST** /system/info.json | Gets user or project info by API key.



## systemInfo

> SystemInfo200Response systemInfo()

Gets user or project info by API key.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.SystemApi();


apiInstance.systemInfo().then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters

This endpoint does not need any parameter.

### Return type

[**SystemInfo200Response**](SystemInfo200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

