# UniOne.UnsubscribedSet200Response

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**status** | [**SuccessStatusString**](SuccessStatusString.md) |  |  |  true 
**address** | **String** | The unsubscribed email. |  |  true 
**message** | **String** | Unsubscription process details:<br><br>* **unsubscribed** if email has just been unsubscribed,* **was inactive** if it was inactive due some reason,* **was unsubscribed** if it already was unsubscribed before the call,* **added and unsubscribed** if it's a new email without status history and it was added and then unsubscribed immediately. |  |  true 



## Enum: MessageEnum


* `unsubscribed` (value: `"unsubscribed"`)

* `was inactive` (value: `"was inactive"`)

* `was unsubscribed` (value: `"was unsubscribed"`)

* `added and unsubscribed` (value: `"added and unsubscribed"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




