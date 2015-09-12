## Error Response

> Sample Response

```json
{
    "status": 403,
    "developer_message": "Invalid access request",
    "more_info_url": "https://docs.fabriq.io/#errors"
}
```

ATTRIBUTES ||
---------------- | -----------  
status<br>**required**	| HTTP status code
developer_message<br>**required** | Error details for the developer
client_message<br>*optional* | Message that may be displayed to the end user
more_info_url<br>*optional* | Documentation URL for more information that may help resolve the error
