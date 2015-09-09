## The alert object
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
    "canceled_date": 1440975513777
}
```

ATTRIBUTES||
---------:        | -----------
uid <br>*string*   | Unique identifier for the alert
type <br>*string*  | Type of the alert. Possible values `panic`
latitude <br>*double*  | Latitude where alert was triggered
longitude <br>*double*  | Longitude where alert was triggered
activity_uid <br>*string*  | Activity associated with this alert
alert_date <br>*timestamp*  | Timestamp (UTC) when alert was triggered
acknowledged <br>*boolean*  | Aert has been acknowledged by at least one contact
canceled <br>*boolean*  | Flag to indicate if this alert has been canceled
canceled_date <br>*timestamp*  | Timestamp (UTC) when alert was canceled
