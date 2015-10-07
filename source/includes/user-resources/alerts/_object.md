## The alert object

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
    "alert_date": 1442763924433,
    "acknowledged": false,
    "canceled": false,
    "canceled_date": null,
    "contacts": ["46b9f6da5da311e5936420c9d07e7899"]
}
```

ATTRIBUTES||
---------:        | -----------
uid<br>*string*   | Unique identifier of the alert
type<br>*string*  | Type of the alert. Possible values `panic`, `notification`, `timeout`, `ping`, `start_activity`, `end_activity`
latitude<br>*double*  | Latitude where alert was triggered
longitude<br>*double*  | Longitude where alert was triggered
floor<br>*integer*  | If indoors, floor of the venue<br>*Street level (ground floor) is 0*
device<br>*string*  | Device uid associated with this alert
activity<br>*string*  | Activity uid associated with this alert
alert_date<br>*timestamp*  | Timestamp (UTC) when alert was triggered
acknowledged<br>*boolean*  | Alert has been acknowledged by at least one contact
canceled<br>*boolean*  | Flag to indicate if this alert has been canceled
canceled_date<br>*timestamp*  | Timestamp (UTC) when alert was canceled
contacts<br>*array*  | List of contacts notified by this alert
