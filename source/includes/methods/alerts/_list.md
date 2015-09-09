## List active alerts

> Definition

```text
GET https://api.fabriq.io/alerts
```

> Sample Request

```shell
curl 'https://api.fabriq.io/alerts/panic'    \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> Sample Response

```json
[{
    "uid": "8d3dd9ed-146e-4526-a69b-d06c7d12cbf9",
    "type": "panic",
    "latitude": 40.01592844038895,
    "longitude": -105.2487217142231,
    "activity_uid": null,
    "alert_date": 1440975513777,
    "acknowledged": true,
    "canceled": false
}]
```

### Returns
An array of alert objects or an empty array if no active alerts were found.
