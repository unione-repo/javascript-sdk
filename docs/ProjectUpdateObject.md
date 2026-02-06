# UniOne.ProjectUpdateObject

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**name** | **String** | Project name, unique for user account. |  |  true 
**country** | **String** | ISO-3166 alpha-2 country code. If set, UniOne treats project personal data according to country laws, e.g. GDPR for european countries. |  | 
**sendEnabled** | **Boolean** | Whether email sending is enabled for this project or not. | [default to true] | 
**customUnsubscribeUrlEnabled** | **Boolean** | If it's false then UniOne adds default unsubscribe footer to each email sent with API key of the project. If it's true then appending default unsubscribe footer for this project is avoided and sending with custom unsubscribe url or even without unsubscribe url is permitted for the project. Please note that custom_unsubscribe_url_enabled=true is available only if removing unsubscribe link is approved for the user account by support. More on this [here](https://docs.unione.io/en/unsubscribe-link). When custom_unsubscribe_url_enabled is skipped on creating a project, it's value is taken from user |  | 
**backendDomainId** | **Number** | A unique domain identifier which will determine the [tracking domain](https://docs.unione.io/en/tracking-domains) or [dedicated IP](/dedicated-ip) pool to be used by default. If the value is not specified, a default backend domain will be assigned for your account or project instead. |  | 
**unsubscribePageId** | **Number** | A unique identifier that defines the default unsubscribe page. If absent, the account/project will be assigned the system default unsubscribe page. |  | 
**emailCounter** | **Number** | Project's email counter value. 0 value only is accepted (which means resetting the counter to zero), or refreshes automatically depending on the counter mode set with the 'email_counter_mode' parameter. If the request doesn't contain the field or contains null, the limit value doesn't change. |  | 
**emailCounterLimit** | **Number** | Allows you to limit the number of emails sent by the project. The sending stops when the limit is reached. Any non-negative 64-bit integer is acceptable. Setting to 0 means no limit. If the request doesn't contain the field or contains null, the limit value doesn't change. | [default to 0] | 
**emailCounterMode** | **String** | Sets the email counter mode. It allows you to choose whether the counter should reset automatically, or remain permanent. The following values are acceptable: 'default' - the counter resets to zero automatically at the beginning of each accounting period, 'permanent' - the counter never resets automatically. The reset can be done only manually by the user in the request with the passes 0 value in the email_counter field. If the request doesn't contain the field or contains a null value, the limit value doesn't change. | [default to &#39;default&#39;] | 



## Enum: EmailCounterModeEnum


* `default` (value: `"default"`)

* `permanent` (value: `"permanent"`)

* `unknown_default_open_api` (value: `"unknown_default_open_api"`)




