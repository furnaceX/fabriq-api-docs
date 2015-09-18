## Trigger a PANIC alert

> Definition

```text
POST https://api.fabriq.io/alerts/panic
```

> Sample Request

```shell
curl -X POST 'https://api.fabriq.io/alerts/panic'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
        "latitude": 40.01592844038895,                    
        "longitude": -105.2487217142231                  
       }'
```

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
    "canceled": false
}
```

ARGUMENTS ||
---------:        | -----------
activity_uid <br>*optional*  | Activity associated with this alert
latitude <br>*optional*  | Latitude where alert was triggered
longitude <br>*optional*  | Longitude where alert was triggered


### Returns
An alert object if messages were successfully sent to the user's contact(s).
