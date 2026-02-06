# UniOne.SystemInfo200Response

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**status** | [**SuccessStatusString**](SuccessStatusString.md) |  |  |  true 
**userId** | **Number** | Unique user identifier. |  |  true 
**email** | **String** | Email of the user. |  |  true 
**projectId** | **String** | Unqiue project identifier, ASCII string up to 36 characters long. Present only if the API key used for request is the project API key. |  | 
**projectName** | **String** | Project name, unique for user account. Present only if the API key used for request is the project API key. |  | 
**projectAccounting** | [**ProjectAccountingObject**](ProjectAccountingObject.md) |  |  | 
**accounting** | [**SystemInfo200ResponseAccounting**](SystemInfo200ResponseAccounting.md) |  |  | 


