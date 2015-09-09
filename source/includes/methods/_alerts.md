# Alerts

## The alert object

```json
{
    "uid": "8d3dd9ed-146e-4526-a69b-d06c7d12cbf9",
    "type": "panic",
    "latitude": 40.01592844038895,
    "longitude": -105.2487217142231,
    "activity_uid": null,
    "alert_date": 1440975513777,
    "acknowledged": true,
    "enabled": true,
    "canceled": false
}
```

ATTRIBUTES||
---------:        | -----------
uid <br>*string*   | Unique identifier for the alert
type <br>*string*  | Type of the alert. Possible values `panic`
latitude <br>*double*  | Latitude where alert was triggered
longitude <br>*double*  | Longitude where alert was triggered
activity_uid <br>*string*  | UID of activity in progress when alert was triggered
alert_date <br>*string*  | Timestamp (UTC) when alert was triggered
enabled <br>*boolean*  | Flag to indicate if this alert is still active
canceled <br>*boolean*  | Flag to indicate if this alert is still active



## Panic

### HTTP Request
`POST https://api.fabriq.io/alerts/panic`


Parameter | Description
--------- | -----------
username  | username of account holder. This will return true is the username is available for assignment.
