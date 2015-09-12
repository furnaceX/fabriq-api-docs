## Update position

> Definition

```text
POST https://api.fabriq.io/activities/{ACTIVITY_UID}/position
```

> Sample Request

```shell
curl -X POST 'https://api.fabriq.io/activities/191e9aee-58e1-11e5-a0dd-38c98601185b/position'  \
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
HTTP Status Code: 201
```

ARGUMENTS ||
---------:| -----------
positions <br>**required**  | An array of [position](#position) objects. `latitude`, `longitude` and `timestamp` fields are required.



### Returns
This method will return a 201 HTTP Status code if the data was uploaded successfully.  It does not return a JSON object.
