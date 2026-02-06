# UniOne.SystemInfo200ResponseAccounting

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**periodStart** | **String** | Date and time of accounting period start in UTC in **YYYY-MM-DD hh:mm:ss** format. |  |  true 
**periodEnd** | **String** | Date and time of accounting period end in UTC in **YYYY-MM-DD hh:mm:ss** format. |  |  true 
**emailsIncluded** | **Number** | Number of emails included into accounting period. |  |  true 
**emailsSent** | **Number** | Number of emails sent during accounting period. Can be bigger than emails_included in case of overage. |  |  true 


