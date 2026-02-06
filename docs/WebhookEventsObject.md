# UniOne.WebhookEventsObject

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**spamBlock** | **[String]** | If present then spam block events will be reported. Should contain single array element with ***** string. |  | 
**emailStatus** | **[String]** | If present then email status change events will be reported. Contains names of statuses to notify of. |  | 



## Enum: [EmailStatusEnum]


* `sent` (value: `"sent"`)

* `delivered` (value: `"delivered"`)

* `opened` (value: `"opened"`)

* `clicked` (value: `"clicked"`)

* `unsubscribed` (value: `"unsubscribed"`)

* `subscribed` (value: `"subscribed"`)

* `soft_bounced` (value: `"soft_bounced"`)

* `hard_bounced` (value: `"hard_bounced"`)

* `spam` (value: `"spam"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




