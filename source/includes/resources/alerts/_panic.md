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
    "activity_uid": null,
    "alert_date": 1442763924433,
    "acknowledged": false,
    "canceled": false,
    "canceled_date": null
}
```

ARGUMENTS ||
---------:        | -----------
activity_uid<br>*optional*, *string*  | Activity associated with this alert
latitude<br>*optional*, *double*  | Latitude where alert was triggered
longitude<br>*optional*, *double*  | Longitude where alert was triggered


### Returns
An alert object if messages were successfully sent to the user's contact(s).