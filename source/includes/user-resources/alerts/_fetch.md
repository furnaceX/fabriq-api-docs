## Retrieve an alert

> **Definition**

```text
GET https://api.fabriq.io/alerts/{ALERT_UID}
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/alerts/5c2e0f1b0ce94b7ea75104a2ef022529'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> **Sample Response**

```json
{
    "uid": "5c2e0f1b0ce94b7ea75104a2ef022529",
    "type": "panic",
    "latitude": 40.01592844038895,
    "longitude": -105.2487217142231,
    "floor": null,
    "device": null,
    "activity": null,
    "alert_date": 1442763924000,
    "acknowledged": true,
    "canceled": false,
    "canceled_date": null
}
```

ARGUMENTS  ||
---------: | -----------
alert_uid<br>**required**, *string*  | The UID of the alert to be retrieved


### Returns
An alert object if a valid UID was provided.
