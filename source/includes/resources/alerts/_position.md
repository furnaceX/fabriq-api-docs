## Update position

> Definition

```text
POST https://api.fabriq.io/alerts/{ALERT_UID}/position
```

> Sample Request

```shell
curl -X POST 'https://api.fabriq.io/alerts/8d3dd9ed-146e-4526-a69b-d06c7d12cbf9/position'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -H 'Content-Type: application/json'         \
  -d '[{                                        
            "latitude": 40.01547488387676,
            "longitude":-105.2499169484761,
            "timestamp": 1401640190777                      
       },{                                      
            "latitude": 40.0154335191846,                    
            "longitude": -105.2499519010123,                    
            "timestamp": 1401640196770                      
       }]'
```


> Sample Response

```text
{
    "count": 2
}
```

ARGUMENTS ||
---------:| -----------
positions <br>**required**  | An array of [position](#position) objects. `latitude`, `longitude` and `timestamp` fields are required.



### Returns
This method returns an object with the number of positions uploaded.
