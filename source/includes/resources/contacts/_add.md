## Add a contact

> Definition

```text
POST https://api.fabriq.io/contacts
```

> Sample Request

```shell
curl -X POST 'https://api.fabriq.io/contacts'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
         "first_name": "Jane",                    
         "last_name": "Doe",                    
         "email": "jane@example.com",                    
         "mobile_number": "+12125551313",
         "circles": ["d4826772-542f-11e5-9364-20c9d07e7899"]

      }'
```

> Sample Response

```json
{
    "uid": "761d4f1a-a121-40f8-a8d3-2993ba5861d9",
    "first_name": "Jane",
    "last_name": "Doe",
    "display_name": "Jane doe",
    "photo_url": null,
    "email": " jane@example.com",
    "mobile_number": "+12125551313",
    "email_alert": false,
    "sms_alert": false,
    "push_alert": false,
    "email_verified": false,
    "mobile_verified": false,
    "circles":[{
        "uid": "d4826772-542f-11e5-9364-20c9d07e7899",
        "photo_url": null,
        "display_name": "Default"
    }]
}
```

ARGUMENTS ||
---------:        | -----------
first_name <br>**required**  | Contact's first name
last_name <br>**required**  | Contact's last name
mobile_number <br>**required**  | Contact's mobile number  ([E.164 format](https://en.wikipedia.org/wiki/E.164))
email <br>*optional*  | Contact's email address
circles <br>*optional*  | Array of `circle_uid`'s to which this contact should belong. If not specified, contact will be added to the user's default circle.
photo_data <br>*optional*  |  -
photo_content_type <br>*optional*  |  -
photo_size <br>*optional*  |  -


### Returns
A contact object.
