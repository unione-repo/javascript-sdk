# UniOne.DomainGetDnsRecords200Response

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**status** | [**SuccessStatusString**](SuccessStatusString.md) |  |  |  true 
**domain** | **String** | Domain to get DNS records for. |  |  true 
**verificationRecord** | **String** | Record to be added **as is** to verify ownership of this domain. |  |  true 
**dkim** | **String** | DKIM signature for the domain. This property contains only the key part, you should prepend it with **k=rsa, p=** part for the record to be valid (see example). |  |  true 


