# UniOne.DomainList200ResponseDomainsInnerDkim

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**key** | **String** | DKIM signature for the domain. This property contains only the key part, you should prepend it with **k=rsa, p=** part for the record to be valid (see [domain/get-dns-records](https://docs.unione.io/en/web-api-ref#domain-get-dns-records)). |  | 
**status** | **String** | Only domains with **active** DKIM record are allowed as sender domains. |  | 



## Enum: StatusEnum


* `active` (value: `"active"`)

* `inactive` (value: `"inactive"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




