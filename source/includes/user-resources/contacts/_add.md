## Add a contact

> **Definition**

```text
POST https://api.fabriq.io/contacts
```

> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/contacts'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
         "first_name": "Jane",                    
         "last_name": "Doe",                    
         "email": "jane@example.com",                    
         "mobile_number": "+12125551313",
         "circles": ["039d2aa25d4e11e5a0dd38c98601185b"]

      }'
```

> **Sample Response**

```json
{
    "uid": "836bba12589e46d5b2c690c749e2e230",
    "first_name": "Jane",
    "last_name": "Doe",
    "display_name": "Jane doe",
    "nickname": null,
    "relationship": null,
    "photo_url": null,
    "email": " jane@example.com",
    "mobile_number": "+12125551313",
    "email_alert": false,
    "sms_alert": false,
    "push_alert": false,
    "email_verified": false,
    "mobile_verified": false,
    "circles":[{
        "uid": "039d2aa25d4e11e5a0dd38c98601185b",
        "photo_url": null,
        "display_name": "Default"
    }]
}
```

ARGUMENTS ||
---------:        | -----------
first_name<br>**required**, *string* | Contact's first name
last_name<br>**required**, *string*  | Contact's last name
mobile_number<br>**required**, *string*  | Contact's mobile number  ([E.164 format](https://en.wikipedia.org/wiki/E.164))
nickname<br>*optional*, *string*  | Contact's nickname
relationship<br>*optional*, *string*  | Contact's relationship to the user
email<br>*optional*, *string*  | Contact's email address
circles<br>*optional*, *array*  | Array of `circle_uid`'s to which this contact should belong. If not specified, contact will be added to the user's default circle.


### Returns
A contact object.
