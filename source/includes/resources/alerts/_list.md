## List active alerts

> **Definition**

```text
GET https://api.fabriq.io/alerts
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/alerts'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> **Sample Response**

```json
[{
    "uid": "5c2e0f1b0ce94b7ea75104a2ef022529",
    "type": "panic",
    "latitude": 40.01592844038895,
    "longitude": -105.2487217142231,
    "device": null,
    "activity": null,
    "alert_date": 1440975513777,
    "acknowledged": true,
    "canceled": false
}]
```

### Returns
An array of alert objects or an empty array if no active alerts were found for this user.
