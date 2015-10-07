## Create a notification

> **Definition**

```text
POST https://api.fabriq.io/app/notifications
```

> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/app/notifications'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
        "name": "Campus Escort",
        "message": "Requesting an escort to walk home.",
        "cancel_message": "Escort no longer needed. Thank you.",
        "pin_required": true
      }'
```

> **Sample Response**

```json
{
    "uid": "68a6e7fe5f324e048ea2f2b29271f895",
    "name": "Campus Escort",
    "message": "Requesting an escort to walk home.",
    "cancel_message": "Escort no longer needed. Thank you.",
    "pin_required": true,
    "priority": 10,
    "description": null
}
```

ARGUMENTS ||
---------:        | -----------
name<br>**required**, *string*  | Notification name
message<br>**required**, *string*  | Default message sent to the user's contacts
cancel_message<br>*optional*, *string*  | If set, allows this notification to be "canceled" with this message sent to the user's contacts
pin_required<br>*optional*, *boolean*  | If true, the notification can only be canceled with a PIN
priority<br>*optional*, *integer*  | Relative priority of this notification relative to others defined by your app.<br>*Default is 10*
description<br>*optional*, *string*  | A description for this notification



### Returns
A notification object.  Use the returned `uid` to [trigger the notification](#trigger-a-notification).
