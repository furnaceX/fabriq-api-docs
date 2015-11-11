## The alert object

> **Sample Response**

```json
{
    "uid": "68a6e7fe5f324e048ea2f2b29271f895",
    "name": "Campus Escort",
    "message": "Requesting an escort to walk home.",
    "cancel_message": "Escort no longer needed. Thank you.",
    "cancellable": true,
    "pin_required": true,
    "priority": 10,
    "description": null
}
```

ATTRIBUTES||
---------:        | -----------
name<br>*string*  | Notification name
message<br>*string*  | Default message sent to the user's contacts
cancel_message<br>*optional*, *string*  | Default cancel message sent to the user's contacts
cancellable<br>*optional*, *boolean*  | If set to true, allows the alert to be "canceled"
pin_required<br>*boolean*  | If true, the alert can only be canceled with a PIN
priority<br>*integer*  | Relative priority of this alert relative to others defined by your app.<br>*Default is 10*
description<br>*string*  | A description for this alert
