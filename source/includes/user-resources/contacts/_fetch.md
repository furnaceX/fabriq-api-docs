## Retrieve a contact

> **Definition**

```text
GET https://api.fabriq.io/contacts/{CONTACT_UID}
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/contacts/46b9f6da5da311e5936420c9d07e7899' \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"
```

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


ARGUMENTS  ||
---------: | -----------
contact_uid<br>**required**, *string*  | UID of the contact to be retrieved


### Returns
A contact object.
