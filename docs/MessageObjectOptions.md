# UniOne.MessageObjectOptions

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**sendAt** | **String** | Date and time in **YYYY-MM-DD hh:mm:ss** format in the UTC timezone. Allows schedule sending up to 24 hours in advance. |  | 
**unsubscribeUrl** | **String** | Custom unsubscribe link. Read more [here](https://docs.unione.io/en/unsubscribe-link). |  | 
**customBackendId** | **Number** | Backend-domain identifier to send message with. If custom_backend_id is not set, default one for your account/project will be used. You can pay for one or more dedicated IPs and use this option. |  | 
**smtpPoolId** | **String** | SMTP pool identifier to send message with. Usually you don't need to pass this parameter because correct smtp_pool_id is selected automatically based on the default one for your account/project or according to custom_backend_id parameter. |  | 


