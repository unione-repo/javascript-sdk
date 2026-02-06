# UniOne.SuppressionList200Response

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**status** | [**SuccessStatusString**](SuccessStatusString.md) |  |  |  true 
**suppressions** | [**[SuppressionListObject]**](SuppressionListObject.md) | Array of suppression objects. |  |  true 
**cursor** | **String** | The parameter indicates from which position the selection is to be started. Must be empty or omitted for the first data chunk. In order to get subsequent chunks, you must set the **cursor** parameter in your request, using the value received in response to the previous request. |  |  true 


