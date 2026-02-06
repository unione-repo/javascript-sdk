# UniOne.WebhookObject

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**id** | **Number** | Webhook unique identifier. |  |  true 
**url** | **String** | Webhook URL. |  |  true 
**status** | [**WebhookStatusString**](WebhookStatusString.md) |  |  |  true 
**eventFormat** | [**WebhookEventFormatString**](WebhookEventFormatString.md) |  |  |  true 
**deliveryInfo** | [**WebhookDeliveryInfoInteger**](WebhookDeliveryInfoInteger.md) |  |  |  true 
**singleEvent** | [**WebhookSingleEventInteger**](WebhookSingleEventInteger.md) |  |  |  true 
**maxParallel** | **Number** | Maximum quantity of permitted parallel queries to your server. The more your server can handle - the better. | [default to 10] |  true 
**updatedAt** | **String** | Webhook properties last update date and time in UTC timezone in **YYYY-MM-DD hh:mm:ss** format. |  | 
**events** | [**WebhookEventsObject**](WebhookEventsObject.md) |  |  | 


