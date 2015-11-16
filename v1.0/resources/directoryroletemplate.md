# directoryRoleTemplate resource type

Represents a directory role template. A directory role template specifies the property values of a directory role ([DirectoryRole](directoryrole.md)). There is an associated directory role template object for each of the directory roles that may be activated in a tenant. To read a directory role or update its members, it must first be activated in the tenant. Only the Company Administrators directory role is activated by default. To activate other available directory roles you send a POST request to the `/directoryRoles` endpoint with the ID of the directory role template on which the directory role is based specified in the **roleTemplateId** parameter of the request. Upon successful completion of this request, you can then start to read and assign members to the directory role. **Note**: A directory role template is exposed for the Users directory role. The Users directory role is implicit and is not visible to directory clients. Every User in the tenant is assigned to this role by the infrastructure. The role is already activated. Do not use this template.


### Methods

| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|[Get directoryRoleTemplate](../api/directoryroletemplate_get.md) | [directoryRoleTemplate](directoryroletemplate.md) |Read properties and relationships of directoryRoleTemplate object.|

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|description|String|The description to set for the directory role. Read-only.|
|displayName|String|The display name to set for the directory role. Read-only. |
|id|String|The unique identifier for the template. Inherited from [DirectoryObject](directoryobject.md). You specify the **id** of the directory role template for the **roleTemplateId** property in the POST request activate a [DirectoryRole](directoryrole.md) in a tenant. Key, Not nullable. Read-only.|

### Relationships
None



### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directoryroletemplate"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryRoleTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->