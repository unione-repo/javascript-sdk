# UniOne.WebhookSetRequest

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**url** | **String** | URL that will receive the notification when an event occurs. The URL should be unique for a user or a project. Only ASCII characters are supported for now in URL, please convert to [Punycode](https://en.wikipedia.org/wiki/Punycode) if you need to use non-ASCII characters. |  |  true 
**status** | [**WebhookStatusString**](WebhookStatusString.md) |  |  | 
**eventFormat** | [**WebhookEventFormatString**](WebhookEventFormatString.md) |  |  | 
**deliveryInfo** | [**WebhookDeliveryInfoInteger**](WebhookDeliveryInfoInteger.md) |  |  | 
**singleEvent** | [**WebhookSingleEventInteger**](WebhookSingleEventInteger.md) |  |  | 
**maxParallel** | **Number** | Maximum quantity of permitted parallel queries to your server. The more your server can handle - the better. | [default to 10] | 
**events** | [**WebhookEventsObject**](WebhookEventsObject.md) |  |  | 


