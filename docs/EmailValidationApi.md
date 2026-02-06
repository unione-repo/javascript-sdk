# UniOne.EmailValidationApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**emailValidationSingle**](EmailValidationApi.md#emailValidationSingle) | **POST** /email-validation/single.json | A maximum of two concurrent requests are allowed; if you send more requests, an error will be returned. Since the verification process should be completed promptly, we've set a time limit on email check. If we encounter a slow email server that does not respond in 5 seconds, you may get an “unknown” status.



## emailValidationSingle

> EmailValidationSingle200Response emailValidationSingle(emailValidationSingleRequest)

A maximum of two concurrent requests are allowed; if you send more requests, an error will be returned. Since the verification process should be completed promptly, we've set a time limit on email check. If we encounter a slow email server that does not respond in 5 seconds, you may get an “unknown” status.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.EmailValidationApi();

let emailValidationSingleRequest = new UniOne.EmailValidationSingleRequest();
emailValidationSingleRequest.setEmail('email@example.com');

apiInstance.emailValidationSingle(emailValidationSingleRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **emailValidationSingleRequest** | [**EmailValidationSingleRequest**](EmailValidationSingleRequest.md)|  |  |  true 

### Return type

[**EmailValidationSingle200Response**](EmailValidationSingle200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

