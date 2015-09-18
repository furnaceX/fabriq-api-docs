## Update current user

> Definition

```text
PUT https://api.fabriq.io/me
```

> Sample Request

```shell
curl -X PUT 'https://api.fabriq.io/me'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
        "mobile_number": "+12155551112"
      }'
```

> Sample Response

```json
{
    "uid": "f3c84161994841c49d729ff97bd0ead0",
    "username": "+12155551112",
    "email": null,
    "mobile_number": "+12155551112",
    "has_contacts": false,
    "is_verified": false,
    "grants": [
        "panic",
        "geoblast"
    ]
}
```


ARGUMENTS ||
---------:        | -----------
uid <br>**required**, *string*  | User identifier
mobile_number <br>*optional*, *string*  | New mobile number ([E.164 format](https://en.wikipedia.org/wiki/E.164))<br>*The user will receive a text message to confirm her mobile number*
email <br>*optional*, *string*  | New email address<br>*The user will receive an email to confirm her email*


### Returns
Return the updated user object. Please note that an update will require
the user to verify his or her email and/or mobile number.
