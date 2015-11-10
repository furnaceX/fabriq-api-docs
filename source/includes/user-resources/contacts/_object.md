## The contact object

> **Sample Response**

```json
{
    "uid": "46b9f6da5da311e5936420c9d07e7899",
    "first_name": "John",
    "last_name": "Doe",
    "display_name": "John Doe",
    "nickname": "Jack",
    "relationship": "Husband",
    "photo_url":null,
    "email": "jdoe@example.com",
    "mobile_number": "+12125551212",
    "email_alert": true,
    "sms_alert": true,
    "push_alert": false,
    "email_verified": true,
    "mobile_verified": true,
    "circles":[{
        "uid": "45778d285da311e5936420c9d07e7899",
        "photo_url": null,
        "display_name": "Default"
    }]
}
```

ATTRIBUTES||
---------:        | -----------
uid<br>*string*   | Unique identifier of the contact
first_name<br>*string*  | Contact's first name
last_name<br>*string*  | Contact's last name
display_name<br>*string*  | Contact's full name
nickname<br>*string*  | Contact's nickname
relationship<br>*string*  | Contact's relationship to user
photo_url<br>*url*  | Link to contact's photo
email<br>*string*  | Contact's email address
mobile_number<br>*string*  | Contact's mobile number  ([E.164 format](https://en.wikipedia.org/wiki/E.164))
email_alert<br>*boolean*  | True if contact has opted to receive email alerts
sms_alert<br>*boolean*  | True if contact has opted to receive text alerts
push_alert<br>*boolean*  | True if contact has opted to receive push alerts
email_verified<br>*boolean*  | True if FABRIQ has verified contact's email address
mobile_verified<br>*boolean*  | True if FABRIQ has verified contact's mobile number
circles<br>*array*  | List of circles to which this contact has been added
