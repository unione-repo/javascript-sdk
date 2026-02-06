# UniOne.WebhookSetJsonPostRequest

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**auth** | **String** | MD5-hash of the message body, in which the value **auth** is replaced by api key of the user/project; with this field the recipient of the notification can both authenticate and verify the notification integrity |  |  true 
**eventsByUser** | [**[WebhookSetJsonPostRequestEventsByUserInner]**](WebhookSetJsonPostRequestEventsByUserInner.md) | Array with only one element, containing events of a user/project. |  |  true 


