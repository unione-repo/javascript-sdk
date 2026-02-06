# UniOne.EmailApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**emailSend**](EmailApi.md#emailSend) | **POST** /email/send.json | Sends an email or a bunch of emails
[**emailSubscribe**](EmailApi.md#emailSubscribe) | **POST** /email/subscribe.json | Sends an email with (re)subscribe link.



## emailSend

> EmailSend200Response emailSend(emailSendRequest)

Sends an email or a bunch of emails

While sending you can provide substitutions (merge tags), use a template, turn on read or click tracking, etc.<br>Restrictions:<br>* maximum request size is 10 MB<br>* maximum number of recipients is 500<br>* The symbol '/' is not allowed in attachment names<br>If the list of recipients contains invalid, non-existent, duplicate, or unsubscribed emails, those emails will be returned in the output parameter failed_emails, and the email will be sent to all other valid emails addresses. If all the emails addresses fall into failed_emails, sending will not be carried out and API error 204 will be returned.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.EmailApi();

let emailSendRequest = new UniOne.EmailSendRequest();
emailSendRequest.setMessage(new UniOne.MessageObject());

apiInstance.emailSend(emailSendRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **emailSendRequest** | [**EmailSendRequest**](EmailSendRequest.md)|  |  |  true 

### Return type

[**EmailSend200Response**](EmailSend200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## emailSubscribe

> SuccessResponse emailSubscribe(emailSubscribeRequest)

Sends an email with (re)subscribe link.

This method allows subscription renewal by a former subscriber who has previously unsubscribed, or who is blocked because of complaints. This method sends an email with a new subscription link to a former subscriber. Once the recipient clicks the link, their subscription status is restored.<br>There is a default restriction that limits this method to being used once a day. If you need to resubscribe more often, please ask support about it.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.EmailApi();

let emailSubscribeRequest = new UniOne.EmailSubscribeRequest();
emailSubscribeRequest.setFromEmail('email@example.com');
emailSubscribeRequest.setFromName('Example');
emailSubscribeRequest.setToEmail('email@example.com');

apiInstance.emailSubscribe(emailSubscribeRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **emailSubscribeRequest** | [**EmailSubscribeRequest**](EmailSubscribeRequest.md)|  |  |  true 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

