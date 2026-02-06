# UniOne.WebhookSetJsonPostRequestEventsByUserInner

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**userId** | **Number** | Unique user identifier. |  |  true 
**projectId** | **String** | Project identifier, present only if webhook was registered for the project using project API key. |  | 
**projectName** | **String** | Project name, present only if webhook was registered for the project using project API key. |  | 
**events** | [**[WebhookSetJsonPostRequestEventsByUserInnerEventsInner]**](WebhookSetJsonPostRequestEventsByUserInnerEventsInner.md) | Array of events reported by webhook. |  |  true 


