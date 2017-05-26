# alert: refresh


### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /alerts/<id>/refresh
POST /providers/<id>/alerts/<id>/refresh
POST /resources/<id>/alerts/<id>/refresh

```
### Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body
In the request body, provide a JSON object with the following parameters.

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|resourceId|String||

### Response
If successful, this method returns `200, OK` response code and [resource](../resources/resource.md) collection object in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "alert_refresh"
}-->
```http
POST https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/alerts/<id>/refresh
Content-type: application/json
Content-length: 38

{
  "resourceId": "resourceId-value"
}
```

##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.resource",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 247

{
  "value": [
    {
      "id": "id-value",
      "originalId": "originalId-value",
      "displayName": "displayName-value",
      "resourceType": "resourceType-value",
      "roleDefinitionCount": 99,
      "roleAssignmentCount": 99
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "alert: refresh",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->"section": "documentation",
  "tocPath": ""
}-->