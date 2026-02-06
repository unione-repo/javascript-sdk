# UniOne.DomainApi

All URIs are relative to https://api.unione.io/en/transactional/api/v1

Method | HTTP request | Description
------------- | ------------- | -------------
[**domainDelete**](DomainApi.md#domainDelete) | **POST** /domain/delete.json | Deletes a domain. Attention: you should use project's API key to delete a project's domain.
[**domainGetDnsRecords**](DomainApi.md#domainGetDnsRecords) | **POST** /domain/get-dns-records.json | Returns info on domain DNS setup for using with UniOne.
[**domainList**](DomainApi.md#domainList) | **POST** /domain/list.json | Returns a list of all registered domains for user or project, together with statuses of last validations.
[**domainValidateDkim**](DomainApi.md#domainValidateDkim) | **POST** /domain/validate-dkim.json | Validates DKIM record for domain.
[**domainValidateVerificationRecord**](DomainApi.md#domainValidateVerificationRecord) | **POST** /domain/validate-verification-record.json | Triggers verification record validation for domain.



## domainDelete

> DomainDelete200Response domainDelete(domainDeleteRequest)

Deletes a domain. Attention: you should use project's API key to delete a project's domain.

Deletes a domain.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.DomainApi();

let domainDeleteRequest = new UniOne.DomainDeleteRequest();
domainDeleteRequest.setDomain('example.com');

apiInstance.domainDelete(domainDeleteRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **domainDeleteRequest** | [**DomainDeleteRequest**](DomainDeleteRequest.md)|  |  |  true 

### Return type

[**DomainDelete200Response**](DomainDelete200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## domainGetDnsRecords

> DomainGetDnsRecords200Response domainGetDnsRecords(domainGetDnsRecordsRequest)

Returns info on domain DNS setup for using with UniOne.

In order to send emails you have to confirm that you own the domain that you are going to send emails from and setup DKIM signature for the domain. This method allows you to register your domain in UniOne and generate verification record and DKIM key, or return previously generated ones if domain is already registered.<br>You should add then DNS records like this to all of the domains you want to confirm:<br>`@ IN TXT **unione-validate-hash=483bb362ebdbeedd755cfb1d4d661**`<br>`us._domainkey IN TXT **k=rsa; p=MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDo7**`<br>`@ IN TXT **v=spf1 include:spf.unione.io ~all**`<br>- First record value should contain **verification-record** field returned by get-dns-records method **as is**.<br>- Second record value should contain **dkim** field value after **p=**. Mind the name of this record! **us._domainkey.** prefix is important for DKIM selector of UniOne to work properly.<br>- Third record contains optional, but very recommended SPF entry. Probably you already have one, then just add append include:spf.unione.io right after v=spf1.<br>Syntax requirements of different DNS providers may differ:<br>- sometimes it's necesarry to put full domain name instead of @ sign.<br>- some providers require add TTL value (like 3600)<br>- some providers don't require quotes for enclosing values<br>Please check requirements of your provider and advice your users to do it.

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.DomainApi();

let domainGetDnsRecordsRequest = new UniOne.DomainGetDnsRecordsRequest();
domainGetDnsRecordsRequest.setDomain('example.com');

apiInstance.domainGetDnsRecords(domainGetDnsRecordsRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **domainGetDnsRecordsRequest** | [**DomainGetDnsRecordsRequest**](DomainGetDnsRecordsRequest.md)|  |  |  true 

### Return type

[**DomainGetDnsRecords200Response**](DomainGetDnsRecords200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## domainList

> DomainList200Response domainList(domainListRequest)

Returns a list of all registered domains for user or project, together with statuses of last validations.

Returns last status of ownership validation and DKIM validation for each domain. Read more [here](https://docs.unione.io/en/web-api-ref#domain).

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.DomainApi();

let domainListRequest = new UniOne.DomainListRequest();
domainListRequest.setDomain('example.com');
domainListRequest.setLimit(null);
domainListRequest.setOffset(null);

apiInstance.domainList(domainListRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **domainListRequest** | [**DomainListRequest**](DomainListRequest.md)|  |  |  true 

### Return type

[**DomainList200Response**](DomainList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## domainValidateDkim

> DomainValidateVerificationRecord200Response domainValidateDkim(domainValidateDkimRequest)

Validates DKIM record for domain.

If you get 200 OK then it means the validation process started succesfully, but it doesn't mean the DKIM record is valid. You should check later dkim.status field returned by [domain/list](https://docs.unione.io/en/web-api-ref#domain-list) method to get the result. Please read more [here](https://docs.unione.io/en/web-api-ref#domain).

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.DomainApi();

let domainValidateDkimRequest = new UniOne.DomainValidateDkimRequest();
domainValidateDkimRequest.setDomain('example.com');

apiInstance.domainValidateDkim(domainValidateDkimRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **domainValidateDkimRequest** | [**DomainValidateDkimRequest**](DomainValidateDkimRequest.md)|  |  |  true 

### Return type

[**DomainValidateVerificationRecord200Response**](DomainValidateVerificationRecord200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## domainValidateVerificationRecord

> DomainValidateVerificationRecord200Response domainValidateVerificationRecord(domainValidateVerificationRecordRequest)

Triggers verification record validation for domain.

If you get 200 OK then it means the validation process started succesfully, but it doesn't mean the verification record is valid. You should check later verification-record.status field returned by [domain/list](https://docs.unione.io/en/web-api-ref#domain-list) method to get the result. Please read more [here](https://docs.unione.io/en/web-api-ref#domain).

### Example

```javascript
import UniOne from '@unione-repo/javascript-sdk';
let defaultClient = UniOne.ApiClient('api.unione.io').instance;
// Configure API key authorization: apiKeyAuth
let apiKeyAuth = defaultClient.authentications['apiKeyAuth'];
apiKeyAuth.apiKey = 'YOUR API KEY';

let apiInstance = new UniOne.DomainApi();

let domainValidateVerificationRecordRequest = new UniOne.DomainValidateVerificationRecordRequest();
domainValidateVerificationRecordRequest.setDomain('example.com');

apiInstance.domainValidateVerificationRecord(domainValidateVerificationRecordRequest).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes | Required
------------- | ------------- | ------------- | ------------- | -------------
 **domainValidateVerificationRecordRequest** | [**DomainValidateVerificationRecordRequest**](DomainValidateVerificationRecordRequest.md)|  |  |  true 

### Return type

[**DomainValidateVerificationRecord200Response**](DomainValidateVerificationRecord200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

