## Remove an alert

> **Definition**

```text
DELETE https://api.fabriq.io/app/alerts/{NOTIFICATION_UID}
```

> **Sample Request**

```shell
curl -X DELETE 'https://api.fabriq.io/alerts/68a6e7fe5f324e048ea2f2b29271f895' \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}'
```

> **Sample Response**

```json
{
    "uid": "68a6e7fe5f324e048ea2f2b29271f895"
}
```

ARGUMENTS  ||
---------: | -----------
alert_uid<br>**required**, *string*  | UID of the alert to be removed<br>*URL parameter*


### Returns
The uid of the alert that was removed.
