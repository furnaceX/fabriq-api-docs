## Report a threat

> **Definition**

```text
POST https://api.fabriq.io/threats
```

> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/threats'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
        "type": "wildlife",                    
        "latitude": 40.00930405724701,
        "longitude": -105.2392134802841,
        "description": "rattlesnake on the path"
       }'
```

> **Sample Response**

```json
{
    "uid": "7ed205f519264529a86014901151dda5",
    "type": "wildlife",
    "level": "medium",
    "test": false,
    "latitude": 40.00930405724701,
    "longitude": -105.2392134802841,
    "address": "1279 Harrison Ct, Boulder, CO 80303, USA",
    "description": "rattlesnake on the path",
    "threat_date": 1442341176384,
    "reported_date": 1442341176384,
    "media": null
}
```

ARGUMENTS ||
---------:        | -----------
type<br>**required**, *string*  | Threat type.  Possible values: `suspicous_person`, `suspicious_object`, `accident`, `road_block`, `road_ice`, `utility`, `weather`, `flood`, `fire`, `wildlife`, `shooting`, `hazardous_material`, `other`
latitude<br>**required**, *double*  | Latitude of the reported threat
longitude<br>**required**, *double*  | Longitude of the reported threat
level<br>*optional*, *string*  |  Threat level.  Possible values: `low`, `medium`, `high`, `severe`.  Default is `medium`
description<br>*optional*, *string*  |  User provided description of the threat
activity<br>*optional*, *string*  |  If an [activity](#activity) is in progress, set its `uid`
test<br>*optional*, *boolean*  |  Indicate this is a test report which should not be displayed to users
anonymous<br>*optional*, *boolean*  |  Indicate that this user wishes to submit this report anonymously
threat_date<br>*optional*, *timestamp*  |  Timestamp when the threat occurred.  Defaults to current time if not known


### Returns
A threat object.
