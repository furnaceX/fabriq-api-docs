## Error Response

> Sample Response

```json
{
    "status": 403,
    "developer_message": "Invalid access request",
    "reference_url": "https://docs.fabriq.io/api/#errors"
}
```

ATTRIBUTES ||
---------------- | -----------  
status<br>**required**	| HTTP status code
developer_message<br>**required** | Error details for the developer
client_message<br>*optional* | Message that may be displayed to the end user
reference_url<br>*optional* | URL for more information that may help resolve the error
