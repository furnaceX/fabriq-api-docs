## List all alerts

> **Definition**

```text
GET https://api.fabriq.io/app/alerts
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/app/alerts'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}'
```

> **Sample Response**

```json
[{
    "uid": "68a6e7fe5f324e048ea2f2b29271f895",
    "name": "Campus Escort",
    "message": "Requesting an escort to walk home.",
    "cancel_message": "Escort no longer needed. Thank you.",
    "cancellable": true,
    "pin_required": true,
    "priority": 10,
    "description": null
}]
```

List all alerts defined by your app.

### Returns
An array of notifications.
