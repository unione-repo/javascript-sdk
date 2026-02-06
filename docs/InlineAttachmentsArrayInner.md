# UniOne.InlineAttachmentsArrayInner

## Properties

Name | Type | Description | Notes | Required
------------ | ------------- | ------------- | ------------- | -------------
**type** | **String** | Attachment type, see [MIME](https://en.wikipedia.org/wiki/MIME). If unsure, use **application/octet-stream**. |  |  true 
**name** | **String** | Attachment content id. For example, **name**=**IMAGECID1** should be referenced in HTML like <img src=**cid:IMAGECID1**>. |  |  true 
**content** | **Blob** | File contents in [base64](https://en.wikipedia.org/wiki/Base64). Maximum file size 7MB (9786710 bytes in base64). |  |  true 


