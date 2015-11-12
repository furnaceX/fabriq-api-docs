## Update contact

> **Definition**

```text
PUT https://api.fabriq.io/contacts/{CONTACT_UID}
```

> **Sample Request**

```shell
curl -X PUT 'https://api.fabriq.io/contacts/836bba12589e46d5b2c690c749e2e230'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
      "nickname": "Jane",                    
      "relationship": "Wife",                    
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
    "nickname": "Jane",
    "relationship": "Wife",
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
contact_uid<br>**required**, *string* | UID of the contact to be updated<br>*URL parameter*
first_name<br>*optional*, *string* | Contact's first name
last_name<br>*optional*, *string*  | Contact's last name
nickname<br>*optional*, *string*  | Contact's nickname
relationship<br>*optional*, *string*  | Contact's relationship to the user
mobile_number<br>*optional*, *string*  | Contact's mobile number  ([E.164 format](https://en.wikipedia.org/wiki/E.164))<br>*A verification text message will be sent to the new mobile number.*
email<br>*optional*, *string*  | Contact's email address<br>*A verification email will be sent to the new email address*
circles<br>*optional*, *array*  | Array of `circle_uid`'s to which this contact should belong.


### Returns
Return the updated contact object.
