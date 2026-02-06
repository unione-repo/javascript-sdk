# UniOne.MessageObjectRecipientsInner

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**email** | **String** | Recipient email |  |  true 
**substitutions** | **{String: String}** | Object to pass the substitutions(merge tags) for the recipient (e.g. recipient name, discount code, password change link, etc. See [Template engines](https://docs.unione.io/en/template-engines)). The substitutions can be used in the following parameters:<br><br>* body.html* body.plaintext* body.amp* subject* from_name* headers[**List-Unsubscribe**]* options.unsubscribe_url<br><br>A substitution name can consist from latin characters, numbers and **_** symbol, and should start with the letter. There's a special substitution **to_name** which is used to put recipent's name like **Name Surname** to include it to SMTP header **To** in the form **Name Surname <email@example.com>**. The **to_name** length is limited to 78 symbols. |  | 
**metadata** | **{String: String}** | Object for passing the metadata, such as **key**: **value**. Max key quantity: 10. Max key length: 64 symbols. Max value length: 1024 symbols. The metadata is returned by [webhook](https://docs.unione.io/en/web-api-ref#webhook) and [event-dump](https://docs.unione.io/en/web-api-ref#event-dump) methods. If you pass strign up to 128 bit with **campaign_id** field name (name is configurable thru support), it will be considered as campaign identifier in statistics. |  | 


