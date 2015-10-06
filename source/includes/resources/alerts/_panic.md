## Trigger a PANIC alert

> **Definition**

```text
POST https://api.fabriq.io/alerts/panic
```

> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/alerts/panic'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
        "latitude": 40.01592844038895,                    
        "longitude": -105.2487217142231                  
       }'
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
    "alert_date": 1442763924433,
    "acknowledged": false,
    "canceled": false,
    "canceled_date": null
}
```

ARGUMENTS ||
---------:        | -----------
device<br>*optional*, *string*  | Device that triggered this alert
activity<br>*optional*, *string*  | Activity associated with this alert
latitude<br>*optional*, *double*  | Latitude where alert was triggered
longitude<br>*optional*, *double*  | Longitude where alert was triggered
floor<br>*optional*, *integer*  | If indoors, floor of the venue<br>*Street level (ground floor) is 0*


### Returns
An alert object if messages were successfully sent to the user's contact(s).
