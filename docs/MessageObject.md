# UniOne.MessageObject

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**recipients** | [**[MessageObjectRecipientsInner]**](MessageObjectRecipientsInner.md) | Contains recipient emails, substitutions(merge tags) and metadata. |  |  true 
**templateId** | **String** | Optional identifier of the template that had been created by [template/set](https://docs.unione.io/en/web-api-ref#template-set) method. If template_id is passed then fields from the template are used instead of missed email/send parameters. E.g. if **body** parameter in email/send is omitted, **body** from template will be used. If **subject** in email/send is omitted, **subject** from template will be used. |  | 
**tags** | **[String]** | An array of strings. The maximum string length is 50 characters. You can include up to 4 strings which must be unique. No more than 10 000 tags are allowed per project; if you try to add more, email/send will return an error. You may use tags to categorize emails by your own criteria, and they will be passed along by event-dump methods. |  | 
**skipUnsubscribe** | **Number** | Whether to skip or not appending default unsubscribe footer. 1=skip, 0=append, default is 0. You should [ask support](https://cp.unione.io/en/support) to approve<br>usage of skip_unsubscribe=1. [Read more](https://docs.unione.io/en/unsubscribe-link). |  | 
**globalLanguage** | **String** | The language of the unsubscribe footer and unsubscribe page. Languages supported are: **be**, **de**, **en**, **es**, **fr**, **it**, **pl**, **pt**, **ru**, **ua**, **kz**. |  | 
**templateEngine** | [**TemplateEngineString**](TemplateEngineString.md) |  |  | 
**globalSubstitutions** | **{String: String}** | Object for passing the substitutions(merge tags) common for all recipients - e.g., company name. If the substitution names are duplicated in object **substitutions**, the values of the variables will be taken from the object **substitutions**. The substitutions can be used in the following parameters:<br><br>* body.html* body.plaintext* body.amp* subject* from_name* options.unsubscribe_url<br><br>A substitution name can consist from latin characeters, numbers and **_** symbol, and should start with the letter. |  | 
**globalMetadata** | **{String: String}** | Object for passing the metadata common for all the recipients, such as **key**: **value**. Max key quantity: 10. Max key length: 64 symbols. Max value length: 1024 symbols. The metadata is returned by [webhook](https://docs.unione.io/en/web-api-ref#webhook). To group single emails into a campaign, you can use the system key 'campaign_id' with a value in the form of a non-negative decimal integer up to 128 bits or a UUID in the format 'c7703772-453e-4c77-a9ae-9a1b94051b5a'. Incorrect values will be treated as '0'. |  | 
**body** | [**BodyObject**](BodyObject.md) |  |  |  true 
**subject** | **String** | Email subject. |  |  true 
**fromEmail** | **String** | Sender's email. Required only if template_id parameter is empty. |  | 
**fromName** | **String** | Sender's name. |  | 
**replyTo** | **String** | Optional Reply-To email (in case it's different to sender's email) |  | 
**replyToName** | **String** | Optional Reply-To name (if reply_to email is specified and you want to display not only this email but also the name) |  | 
**trackLinks** | [**TrackLinksInteger**](TrackLinksInteger.md) |  |  | 
**trackRead** | [**TrackReadInteger**](TrackReadInteger.md) |  |  | 
**bypassGlobal** | [**BypassGlobalInteger**](BypassGlobalInteger.md) |  |  | 
**bypassUnavailable** | [**BypassUnavailableInteger**](BypassUnavailableInteger.md) |  |  | 
**bypassUnsubscribed** | [**BypassUnsubscribedInteger**](BypassUnsubscribedInteger.md) |  |  | 
**bypassComplained** | [**BypassComplainedInteger**](BypassComplainedInteger.md) |  |  | 
**idempotenceKey** | **String** | A string of up to 64 characters containing a unique message key. This can be used to prevent occasional message duplicates. If you send another API request with the same message key within the next minute, it will be declined. We can generate a message key for each letter automatically; to enable this option, please contact our [tech support](https://cp.unione.io/en/support). |  | 
**headers** | [**HeadersObject**](HeadersObject.md) |  |  | 
**attachments** | [**[AttachmentsArrayInner]**](AttachmentsArrayInner.md) | Optional array of attachments |  | 
**inlineAttachments** | [**[InlineAttachmentsArrayInner]**](InlineAttachmentsArrayInner.md) | Optional array of inline attachments, e.g. for including images in email instead of loading them from external URL. |  | 
**options** | [**MessageObjectOptions**](MessageObjectOptions.md) |  |  | 



## Enum: SkipUnsubscribeEnum


* `0` (value: `0`)

* `1` (value: `1`)

* `unknown_default_open_api` (value: `11184809`)




