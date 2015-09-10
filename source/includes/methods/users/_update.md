## Update current user

> Definition

```text
PUT https://api.fabriq.io/me
```

> Sample Request

```shell
curl -X PUT 'https://api.fabriq.io/me'        \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -H 'Content-Type: application/json'         \
  -d '{                                        
        "uid": "0001440886991323-a2d5c77b67d7-0001",
        "mobile_number": "+12155551112"
      }'
```

> Sample Response

```json
{
    "uid": "0001440886991323-a2d5c77b67d7-0001",
    "username": "test01",
    "email": null,
    "mobile_number": "+12155551112",
    "has_contacts": false,
    "is_verified": false,
    "grants":[
        "panic",
        "geoblast",
        "activity_tracking",
        "ping_me",
        "connect_911"
    ]
}
```


ARGUMENTS ||
---------:        | -----------
uid <br>**required**  | User identifier
mobile_number <br>*optional*  | New mobile number ([E.164 format](https://en.wikipedia.org/wiki/E.164))
email <br>*optional*  | New email address


### Returns
Return the updated user object. Please note that an update will require
the user to verify his or her email and/or mobile number.
