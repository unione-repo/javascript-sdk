# UniOne.EmailValidationSingle200Response

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**status** | [**SuccessStatusString**](SuccessStatusString.md) |  |  |  true 
**email** | **String** | Email address to be checked. |  |  true 
**result** | **String** | Possible statuses:<br><br>* **valid** - the address is valid,* **invalid** - the address is invalid,* **suspicious** - the address looks suspicious,* **unknown** - could not perform validation, the domain’s mail server has not responded within the time limit. |  |  true 
**cause** | **String** | Possible statuses:<br><br>* **no_mx_record** - no MX record found for the target domain,* **syntax_error** - the address syntax is invalid,* **possible_typo** - the address is likely to have a typo,* **mailbox_not_found** - the address does not exist,* **global_suppression** - the address has been marked as unreachable due to multiple previous delivery errors,* **disposable** - this is a disposable one-time email address which is usually valid for a few minutes only,* **role** - the address is not likely to belong to an actual person, but rather to a certain business staff role,* **abuse** - the address is known to be a source of a large number of complaints, sometimes issued automatically,* **spamtrap** - this email is a spam trap, it is published openly but never used for actual emails. Sending messages to such addresses has a huge negative impact on reputation score,* **smtp_connection_failed** - the domain’s SMTP server does not respond; the address may contain a typo. |  |  true 
**validity** | **Number** | Validity score, from 0 to 100 (0 – invalid, 100 – valid). |  |  true 
**localPart** | **String** | Local part (everything preceding the @ sign). |  |  true 
**domain** | **String** | Domain name part. |  |  true 
**mxFound** | **Boolean** | True if the address’ domain does have an MX record, false if does not. |  |  true 
**mxRecord** | **String** | Preferred MX record for the domain. |  |  true 
**didYouMean** | **String** | For addresses which are likely to have typing errors (cause=possible_typo), a suggested variant with a fixed typo. |  |  true 
**processedAt** | **String** | Email check date and time, YYYY-MM-DD hh:mm:ss UTC. |  |  true 


