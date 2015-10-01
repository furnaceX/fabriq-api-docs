## The user object

> **Sample Response**

```json
{
    "uid": "9ff6178e851942cbb5a5ddc71f82588d",
    "username": "+12155551111",
    "email": "test@example.com",
    "mobile_number": "+12155551111",
    "has_contacts": true,
    "is_verified": true,
    "grants":[
        "panic",
        "geoblast",
        "breadcrumbs",
        "ping",
        "911"
    ]
}
```

ATTRIBUTES||
---------:        | -----------
uid <br>*string*   | Unique identifier of the user
username <br>*string*  | User's username
email <br>*string*  | User's email address
mobile_number <br>*string*  | User's mobile number ([E.164 format](https://en.wikipedia.org/wiki/E.164))
has_contacts <br>*boolean*  | True if user has at least one verified contact
is_verified <br>*boolean*  | True if FABRIQ has validated user's email and mobile_number
grants <br>*array*  | Array of features enabled for this user. Possible values: `panic`, `geoblast`, `breadcrumbs`, `ping`, `911`
