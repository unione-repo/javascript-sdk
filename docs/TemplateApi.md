# UniOne.TemplateApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**templateDelete**](TemplateApi.md#templateDelete) | **POST** /template/delete.json | Deletes a template by id.
[**templateGet**](TemplateApi.md#templateGet) | **POST** /template/get.json | Gets template properties by it's id.
[**templateList**](TemplateApi.md#templateList) | **POST** /template/list.json | Returns the list of all or some templates of the account.
[**templateSet**](TemplateApi.md#templateSet) | **POST** /template/set.json | Creates or updates an email template.



## templateDelete

> SuccessResponse templateDelete(templateGetRequest)

Deletes a template by id.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.TemplateApi();

let templateGetRequest = new UniOne.TemplateGetRequest();
templateGetRequest.setId('00000000-0000-0000-0000-000000000000');

apiInstance.templateDelete(templateGetRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **templateGetRequest** | [**TemplateGetRequest**](TemplateGetRequest.md)|  |  |  true 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## templateGet

> TemplateSet200Response templateGet(templateGetRequest)

Gets template properties by it's id.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.TemplateApi();

let templateGetRequest = new UniOne.TemplateGetRequest();
templateGetRequest.setId('00000000-0000-0000-0000-000000000000');

apiInstance.templateGet(templateGetRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **templateGetRequest** | [**TemplateGetRequest**](TemplateGetRequest.md)|  |  |  true 

### Return type

[**TemplateSet200Response**](TemplateSet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## templateList

> TemplateList200Response templateList(templateListRequest)

Returns the list of all or some templates of the account.

You can iterate thru large list using **offset** and **limit** parameters. When less than **limit** templates are returned then the end of list is reached.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.TemplateApi();

let templateListRequest = new UniOne.TemplateListRequest();
templateListRequest.setLimit(null);
templateListRequest.setOffset(null);

apiInstance.templateList(templateListRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **templateListRequest** | [**TemplateListRequest**](TemplateListRequest.md)|  |  |  true 

### Return type

[**TemplateList200Response**](TemplateList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## templateSet

> TemplateSet200Response templateSet(templateSetRequest)

Creates or updates an email template.

Restrictions:<br>* The maximum request size is 10 MB.<br>* The number of templates is limited to 10000.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.TemplateApi();

let templateSetRequest = new UniOne.TemplateSetRequest();
templateSetRequest.setTemplate(new UniOne.TemplateObject());

apiInstance.templateSet(templateSetRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **templateSetRequest** | [**TemplateSetRequest**](TemplateSetRequest.md)|  |  |  true 

### Return type

[**TemplateSet200Response**](TemplateSet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

