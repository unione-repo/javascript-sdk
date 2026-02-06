# UniOne.AttachmentsArrayInner

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**type** | **String** | Attachment type, see [MIME](https://en.wikipedia.org/wiki/MIME). If unsure, use **application/octet-stream**. |  |  true 
**name** | **String** | Attachment name in the format: **name.extension**. When multiple attachments are passed, their names must be unique. The symbol ‘/’ is not allowed in attachment names. |  |  true 
**content** | **Blob** | File contents in [base64](https://en.wikipedia.org/wiki/Base64). Maximum file size 7MB (9786710 bytes in base64). |  |  true 


