## Cancel an alert

> Definition

```text
DELETE https://api.fabriq.io/alerts/{ALERT_UID}
```

> Sample Request

```shell
curl -X DELETE 'https://api.fabriq.io/alerts/8d3dd9ed-146e-4526-a69b-d06c7d12cbf9'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -d pin=1234
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
    "canceled": true,
    "canceled_date": 1440975513777
}
```

ARGUMENTS ||
---------:        | -----------
pin <br>**required**  | User's 4-digit PIN

<br/>
<aside class="notice">
The supplied PIN can be either the user's OK PIN or distress PIN.  The OK PIN will actually
cancel the alert while the distress PIN should cause the UI to seem like it has been disabled.
</aside>

### Returns
An alert object with canceled status and date set.  If the distress PIN was entered, the `canceled`
attribute will return `false`.