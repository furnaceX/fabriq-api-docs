## Cancel an alert

> **Definition**

```text
DELETE https://api.fabriq.io/alerts/{ALERT_UID}
```

> **Sample Request**

```shell
curl -X DELETE -G 'https://api.fabriq.io/alerts/5c2e0f1b0ce94b7ea75104a2ef022529'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -d pin=1234
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
    "alert_date": 1440975513777,
    "acknowledged": true,
    "canceled": true,
    "canceled_date": 1440975513777
}
```

> **Sample Error**

```json
{
    "status": 412,
    "developer_message": "Invalid pin: 1212",
    "reference_url": "https://docs.fabriq.io/api"
}
```

ARGUMENTS ||
---------:        | -----------
pin<br>**required**, *string*  | User's 4-digit PIN

<br/>
<aside class="notice">
The supplied PIN can be either the user's OK PIN or duress PIN.  The OK PIN will actually
cancel the alert while the duress PIN should cause the UI to seem like it has been disabled.
</aside>

### Returns
An alert object with canceled status and date set.  If the duress PIN was entered, the `canceled`
attribute will return `false`. If an incorrect PIN was submitted, a 412 HTTP response code will be returned with
an error message.
