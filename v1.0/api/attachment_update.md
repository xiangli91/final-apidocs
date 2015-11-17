# Update attachment

Update the properties of attachment object.
### Prerequisites
One of the following **scopes** is required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/<id>/events/<id>/attachments/<id>
PATCH /groups/<objectId>/events/<id>/attachments/<id>
PATCH /users/<id>/messages/<id>/attachments/<id>
```
### Request headers
| Name       | Type | Description|
|:-----------|:------|:----------|
| Authorization  | string  | Bearer <token>. Required. |

### Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.

| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|contentType|String|The MIME type.|
|isInline|Boolean|`true` if the attachment is an inline attachment; otherwise, `false`.|
|lastModifiedDateTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|name|String|The attachment's file name.|
|size|Int32|The length of the attachment in bytes.|

### Response
If successful, this method returns a `200 OK` response code and updated [attachment](../resources/attachment.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_attachment"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/events/<id>/attachments/<id>
Content-type: application/json
Content-length: 142

{
  "lastModifiedDateTime": "datetime-value",
  "name": "name-value",
  "contentType": "contentType-value",
  "size": 99,
  "isInline": true
}
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
Content-type: application/json
Content-length: 162

{
  "lastModifiedDateTime": "datetime-value",
  "name": "name-value",
  "contentType": "contentType-value",
  "size": 99,
  "isInline": true,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->