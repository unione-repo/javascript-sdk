# UniOne.SuppressionListRequest

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**cause** | **String** | Cause of email being suppressed. One of:<br><br>* __unsubscribed__ - email is unsubscribed;* __temporary_unavailable__ - the email address is unavailable. This means that over the next three days sending to this address will return an error. Email may be temporarily unavailable due to several reasons, e.g.:<br>    1. a previous email has been rejected by the recipient's server for spam;* the recipient's mailbox is full or is not used;* recipient's domain does not accept mail;* sending server was rejected due to blacklisting;* __permanent_unavailable__ - the email address is permanently unavailable due to multiple hard bounces;* __complained__ - the recipient reported spam in the previous emails;* __blocked__ - sending to the email is prohibited by administration of UniOne.<br><br>We may add some new causes in the future. |  | 
**source** | **String** | Source of email being suppressed. One of:<br><br>* __user__ - suppressed by user with [suppression/set](https://docs.unione.io/en/web-api-ref#suppression-set);* __system__ - sending to the email is prohibited by system, for example due to multiple hard bounces;* __subscriber__ - the recipient reported spam or unsubscribed in the previous emails. |  | 
**startTime** | **String** | Date in the format YYYY-MM-DD hh:mm:ss to get suppression list from the **start_time** to the present day. Ignored if **cursor** is not empty. |  | 
**cursor** | **String** | The parameter indicates from which position the selection is to be started. Must be empty or omitted for the first data chunk. In order to get subsequent chunks, you must set the **cursor** parameter in your request, using the value received in response to the previous request. |  | 
**limit** | **Number** | Limits the number of records to be returned at one time, default is 50. |  | 


