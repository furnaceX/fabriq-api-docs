## The user object
> Sample Response

```json
{
    "uid": "0001440886991323-a2d5c77b67d7-0001",
    "username": "+12155551111",
    "email": null,
    "mobile_number": "+12155551111",
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

ATTRIBUTES||
---------:        | -----------
uid <br>*string*   | Unique identifier of the user
username <br>*string*  | User's username
email <br>*string*  | User's email address
mobile_number <br>*string*  | User's mobile number
has_contacts <br>*boolean*  | True if user has at least one verified contact
is_verified <br>*boolean*  | True if FABRIQ has validated user's email and mobile_number
grants <br>*array*  | Array of features enabled for this user
