# UniOne.EmailSend200Response

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**status** | [**SuccessStatusString**](SuccessStatusString.md) |  |  |  true 
**jobId** | **String** | Job identifier, might be useful for investigating errors. |  |  true 
**emails** | **[String]** | Array of recipients emails successfully accepted for sending. |  | 
**failedEmails** | **[{String: String}]** | Object with emails rejected for sending as property names and their statuses as property values, e.g.: {**email1@gmail.com**: **temporary_unavailable**}. Possible statuses:<br><br>* __unsubscribed__ - specified email is unsubscribed;* __invalid__ - the email does not exist or has been entered incorrectly;* __duplicate__ - the email already exists in the request, email duplicating is prevented;* __temporary_unavailable__ - the email address is unavailable. This means that over the next three days sending to this address will return an error. Email may be temporarily unavailable due to several reasons, e.g.:<br>        1. a previous email has been rejected by the recipient's server for spam;* the recipient's mailbox is full or is not used;* recipient's domain does not accept mail;* sending server was rejected due to blacklisting;* __permanent_unavailable__ - the email address is permanently unavailable or unsubscribed globally.* __complained__ - the recipient reported spam in the previous emails;* __blocked__ - sending to the email is prohibited by administration of UniOne.<br><br>We may added new statuses in the future. |  | 


