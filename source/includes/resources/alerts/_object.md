## The alert object

> **Sample Response**

```json
{
    "uid": "5c2e0f1b0ce94b7ea75104a2ef022529",
    "type": "panic",
    "latitude": 40.01592844038895,
    "longitude": -105.2487217142231,
    "device": null,
    "activity": null,
    "alert_date": 1442763924433,
    "acknowledged": false,
    "canceled": false,
    "canceled_date": null
}
```

ATTRIBUTES||
---------:        | -----------
uid <br>*string*   | Unique identifier of the alert
type <br>*string*  | Type of the alert. Possible values `panic`, `timeout`, `ping`, `start_activity`, `end_activity`
latitude <br>*double*  | Latitude where alert was triggered
longitude <br>*double*  | Longitude where alert was triggered
device<br>*string*  | Device uid associated with this alert
activity<br>*string*  | Activity uid associated with this alert
alert_date <br>*timestamp*  | Timestamp (UTC) when alert was triggered
acknowledged <br>*boolean*  | Alert has been acknowledged by at least one contact
canceled <br>*boolean*  | Flag to indicate if this alert has been canceled
canceled_date <br>*timestamp*  | Timestamp (UTC) when alert was canceled
