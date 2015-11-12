## Update an alert

> **Definition**

```text
PUT https://api.fabriq.io/app/alerts/{ALERT_UID}
```

> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/app/alerts/68a6e7fe5f324e048ea2f2b29271f895'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
        "name": "Campus Ride",
        "message": "Requesting a ride to go home.",
        "cancel_message": "Ride no longer needed. Thank you."
      }'
```

> **Sample Response**

```json
{
    "uid": "68a6e7fe5f324e048ea2f2b29271f895",
    "name": "Campus Ride",
    "message": "Requesting a ride to go home.",
    "cancel_message": "Ride no longer needed. Thank you.",
    "cancellable": true,
    "pin_required": true,
    "priority": 10,
    "description": null
}
```

ARGUMENTS ||
---------:        | -----------
alert_uid<br>**required**, *string* | UID of the alert to be updated<br>*URL parameter*
name<br>*optional*, *string*  | Alert name
message<br>*optional*, *string*  | Default message sent to the user's contacts
cancel_message<br>*optional*, *string*  | Default cancel message sent to the user's contacts
cancellable<br>*optional*, *boolean*  | If set to true, allows the alert to be "canceled"
pin_required<br>*optional*, *boolean*  | If true, the alert can only be canceled with a PIN
priority<br>*optional*, *integer*  | Relative priority of this alert relative to others defined by your app.<br>*Default is 10*
description<br>*optional*, *string*  | A description for this alert



### Returns
Return the updated alert object.
