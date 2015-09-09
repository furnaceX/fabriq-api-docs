## Retrieve an alert

> Definition

```text
GET https://api.fabriq.io/alerts/{ALERT_UID}
```

> Sample Request

```shell
curl 'https://api.fabriq.io/alerts/8d3dd9ed-146e-4526-a69b-d06c7d12cbf9'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> Sample Response

```json
{
    "uid": "8d3dd9ed-146e-4526-a69b-d06c7d12cbf9",
    "type": "panic",
    "latitude": 40.01592844038895,
    "longitude": -105.2487217142231,
    "activity_uid": null,
    "alert_date": 1440975513777,
    "acknowledged": true,
    "canceled": false,
    "canceled_date": null
}
```

ARGUMENTS  ||
---------: | -----------
alert_uid <br>**required**  | The UID of the alert to be retrieved


### Returns
An alert object if a valid UID was provided.
