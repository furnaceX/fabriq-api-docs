## List all contacts

> Definition

```text
GET https://api.fabriq.io/contacts
```

> Sample Request

```shell
curl 'https://api.fabriq.io/contacts'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> Sample Response

```json
[{
    "uid": "d621e0d0-542f-11e5-9364-20c9d07e7899",
    "first_name": "John",
    "last_name": "Doe",
    "display_name": "John Doe",
    "photo_url":null,
    "email": "jdoe@example.com",
    "mobile_number": "+12125551212",
    "email_alert": true,
    "sms_alert": true,
    "push_alert": false,
    "email_verified": true,
    "mobile_verified": true,
    "circles":[{
        "uid": "d4826772-542f-11e5-9364-20c9d07e7899",
        "photo_url": null,
        "display_name": "Default"
    }]
},
{
  ...
}]
```

### Returns
An array of contacts or an empty array if the user has not added any contacts yet.
