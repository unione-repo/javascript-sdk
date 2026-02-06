# UniOne.WebhookSetJsonPostRequestEventsByUserInnerEventsInnerEventData

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**jobId** | **String** | Job identifier returned earlier by [email/send](https://docs.unione.io/en/web-api-ref#email-send) method. Property exists only if event_name=**transactional_email_status**. |  | 
**metadata** | **{String: String}** | Metadata passed in [email/send](https://docs.unione.io/en/web-api-ref#email-send) method in recipients.metadata or global_metadata properties. This property exists only if event_name=**transactional_email_status**. |  | 
**email** | **String** | Recipient's email. This property exists only if event_name=**transactional_email_status**. |  | 
**status** | **String** | Email delivery status. This property exists only if event_name=**transactional_email_status**. Possible values are:<br>__accepted__ — the message has been accepted, but not sent yet.<br>__sent__ — the message has been sent, but not delivered yet.<br>__delivered__ — the message has been delivered. It can be changed to “opened”, “clicked”, “unsubscribed”, “subscribed” or “spam”.<br>__opened__ — the message has been delivered and read. It can be changed to “clicked”, “unsubscribed”, “subscribed” or “spam”.<br>__clicked__ — the message has been delivered, read, and at least one of the links in email has been clicked. It can be changed to “unsubscribed”, “subscribed” or “spam”.<br>__unsubscribed__ — the message has been delivered to the recipient and read, but then the recipient unsubscribed. It can be changed to “subscribed”.<br>__subscribed__ — the message has been delivered to the recipient and read, but then the recipient unsubscribed and subscribed again. It can be changed to “unsubscribed”.<br>__soft_bounced__ — temporary delivery failure. UniOne will try to deliver the message during 48 hours. In case of success the status changes to “delivered”, in case of failure to deliver during 48 hours message status changes to “hard_bounced”.<br>__hard_bounced__ — failed to deliver the message, there will be no delivery attempts. It's a final status. There are a lot of possible reasons, you can use SMTP response from delivery_info.destination_response field or UniOne internal reason classification from delivery_info.delivery_status field to analyze the reason.<br>__spam__ — the message has been delivered, but it was reported as spam by the recipient. UniOne can receive and process the spam complaint from several domains, including msn.com, outlook.com, hotmail.com, live.com, ukr.net, yahoo.com, aol.com using [FBL](https://en.wikipedia.org/wiki/Feedback_loop_(email)). |  | 
**eventTime** | **String** | Event date & time in UTC time zone in **YYYY-MM-DD hh:mm:ss** format. This property exists only if event_name=**transactional_email_status**. |  | 
**url** | **String** | URL for **opened** and **clicked** statuses. This property exists only if event_name=**transactional_email_status**. |  | 
**deliveryInfo** | [**WebhookSetJsonPostRequestEventsByUserInnerEventsInnerEventDataDeliveryInfo**](WebhookSetJsonPostRequestEventsByUserInnerEventsInnerEventDataDeliveryInfo.md) |  |  | 
**blockTime** | **String** | Spam block date & time in UTC time zone in **YYYY-MM-DD hh:mm:ss** format. This property exists only if event_name=**transactional_spam_block**. |  | 
**blockType** | **String** | Spam block type, either single or multiple sending SMTP. For single sending SMTP block in common pool UniOne retries several other SMTPs. This property exists only if event_name=**transactional_spam_block**. |  | 
**domain** | **String** | Domain that blocked sending. This property exists only if event_name=**transactional_spam_block**. |  | 
**sMTPBlocksCount** | **Number** | Number of sending SMTPs blocked. This property exists only if event_name=**transactional_spam_block**. |  | 
**domainStatus** | **String** | Whether it's a block or unblock event. This property exists only if event_name=**transactional_spam_block**. |  | 



## Enum: StatusEnum


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





## Enum: BlockTypeEnum


* `one_smtp` (value: `"one_smtp"`)

* `all_smtp` (value: `"all_smtp"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)





## Enum: DomainStatusEnum


* `blocked` (value: `"blocked"`)

* `unblocked` (value: `"unblocked"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




