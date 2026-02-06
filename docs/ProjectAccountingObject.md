# UniOne.ProjectAccountingObject

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**emailCounter** | **Number** | Project's email counter value. It increases on every email sent. |  |  true 
**emailCounterLimit** | **Number** | Allows you to limit the number of emails sent by the project. The sending stops when the limit is reached. Any non-negative 64-bit integer is acceptable. 0 means no limit. |  |  true 
**emailCounterMode** | **String** | 'default' - the counter resets to zero automatically at the beginning of each accounting period. 'permanent' - the counter never resets automatically. | [default to &#39;default&#39;] |  true 



## Enum: EmailCounterModeEnum


* `default` (value: `"default"`)

* `permanent` (value: `"permanent"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




