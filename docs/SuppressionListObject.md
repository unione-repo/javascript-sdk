# UniOne.SuppressionListObject

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**email** | **String** | Email to get suppression details for. |  | 
**cause** | **String** | Cause of email being suppressed. One of:<br><br>* __unsubscribed__ - email is unsubscribed;* __temporary_unavailable__ - the email address is unavailable. This means that over the next three days sending to this address will return an error. Email may be temporarily unavailable due to several reasons, e.g.:<br>    1. a previous email has been rejected by the recipient's server for spam;* the recipient's mailbox is full or is not used;* recipient's domain does not accept mail;* sending server was rejected due to blacklisting;* __permanent_unavailable__ - the email address is permanently unavailable due to multiple hard bounces;* __complained__ - the recipient reported spam in the previous emails;* __blocked__ - sending to the email is prohibited by administration of UniOne.<br><br>We may add some new causes in the future. |  |  true 
**source** | **String** | Source of email being suppressed. One of:<br><br>* __user__ - suppressed by user with [suppression/set](https://docs.unione.io/en/web-api-ref#suppression-set);* __system__ - sending to the email is prohibited by system, for example due to multiple hard bounces;* __subscriber__ - the recipient reported spam or unsubscribed in the previous emails. |  |  true 
**isDeletable** | **Boolean** | Is it possible to delete this suppression by calling suppression/delete method. |  |  true 
**created** | **String** | When suppression was created, in UTC timezone in **YYYY-MM-DD hh:mm:ss** format. |  |  true 


