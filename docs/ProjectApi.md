# UniOne.ProjectApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**projectCreate**](ProjectApi.md#projectCreate) | **POST** /project/create.json | Creates a new project.
[**projectDelete**](ProjectApi.md#projectDelete) | **POST** /project/delete.json | Deletes a project.
[**projectList**](ProjectApi.md#projectList) | **POST** /project/list.json | Lists projects.
[**projectUpdate**](ProjectApi.md#projectUpdate) | **POST** /project/update.json | Updates a project.



## projectCreate

> ProjectCreate200Response projectCreate(projectCreateRequest)

Creates a new project.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.ProjectApi();

let projectCreateRequest = new UniOne.ProjectCreateRequest();
projectCreateRequest.setProject(new UniOne.ProjectObject());

apiInstance.projectCreate(projectCreateRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **projectCreateRequest** | [**ProjectCreateRequest**](ProjectCreateRequest.md)|  |  |  true 

### Return type

[**ProjectCreate200Response**](ProjectCreate200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## projectDelete

> SuccessResponse projectDelete(projectDeleteRequest)

Deletes a project.

The project will be moved to the **trash bin** before being permanently deleted. You can restore the project by contacting support.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.ProjectApi();

let projectDeleteRequest = new UniOne.ProjectDeleteRequest();
projectDeleteRequest.setProjectId('1234567890');
projectDeleteRequest.setProjectApiKey('your api_key');

apiInstance.projectDelete(projectDeleteRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **projectDeleteRequest** | [**ProjectDeleteRequest**](ProjectDeleteRequest.md)|  |  |  true 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## projectList

> ProjectList200Response projectList(projectListRequest)

Lists projects.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.ProjectApi();

let projectListRequest = new UniOne.ProjectListRequest();
projectListRequest.setProjectId('1234567890');
projectListRequest.setProjectApiKey('your api_key');

apiInstance.projectList(projectListRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **projectListRequest** | [**ProjectListRequest**](ProjectListRequest.md)|  |  |  true 

### Return type

[**ProjectList200Response**](ProjectList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## projectUpdate

> ProjectUpdate200Response projectUpdate(projectUpdateRequest)

Updates a project.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.ProjectApi();

let projectUpdateRequest = new UniOne.ProjectUpdateRequest();
projectUpdateRequest.setProjectId('1234567890');
projectUpdateRequest.setProjectApiKey('your api_key');
projectUpdateRequest.setProject(new UniOne.ProjectUpdateObject());

apiInstance.projectUpdate(projectUpdateRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **projectUpdateRequest** | [**ProjectUpdateRequest**](ProjectUpdateRequest.md)|  |  |  true 

### Return type

[**ProjectUpdate200Response**](ProjectUpdate200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

