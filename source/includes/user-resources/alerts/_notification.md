## Trigger a Notification

> **Definition**

```text
POST https://api.fabriq.io/alerts/notifications/{NOTIFICATION_UID}
```

> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/alerts/notifications/68a6e7fe5f324e048ea2f2b29271f895'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
        "latitude": 40.01592844038895,                    
        "longitude": -105.2487217142231,
        "circles": ["dea658b2684d11e5922038c98601185b"]
       }'
```

> **Sample Response**

```json
{
    "uid": "5c2e0f1b0ce94b7ea75104a2ef022529",
    "type": "notification",
    "latitude": 40.01592844038895,
    "longitude": -105.2487217142231,
    "floor": null,
    "device": null,
    "activity": null,
    "alert_date": 1442763924433,
    "acknowledged": false,
    "canceled": false,
    "canceled_date": null,
    "contacts": ["46b9f6da5da311e5936420c9d07e7899"]
}
```

Trigger an [app-defined notification](#create-a-notification).

<br>

ARGUMENTS ||
---------:        | -----------
notification_uid<br>**required**, *string*  | UID of notification to trigger<br>*URL parameter*
circles<br>**required**, *array*  | List of `circle_uid`'s that will be notified when this notification is triggered<br>*The result object contains the list of contacts that were notified*
device<br>*optional*, *string*  | `device_uid` that triggered this notification
activity<br>*optional*, *string*  | `activity_uid` associated with this notification
latitude<br>*optional*, *double*  | Latitude where alert was triggered
longitude<br>*optional*, *double*  | Longitude where alert was triggered
floor<br>*optional*, *integer*  | If indoors, floor of the venue<br>*Street level (ground floor) is 0*



### Returns
An alert object if messages were successfully sent to the user's contact(s).
