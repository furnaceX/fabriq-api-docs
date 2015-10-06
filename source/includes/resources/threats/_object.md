## The threat object

> **Sample Response**

```json
{
    "uid": "7ed205f519264529a86014901151dda5",
    "type": "wildlife",
    "level": "medium",
    "test": false,
    "latitude": 40.00930405724701,
    "longitude": -105.2392134802841,
    "floor": null,
    "address": "1279 Harrison Ct, Boulder, CO 80303, USA",
    "description": null,
    "threat_date": 1442341176000,
    "reported_date": 1442341176000,
    "media":[{
        "uid": "fa4c01b994974daf83e4b121a078f428",
        "url": "https://fabriq.io/files/0218/0250/0215/00524CF105F2B817EEACE7ACE7AFFC17BA26",
        "content_type": "image/jpeg",
        "size": 45950,
        "latitude": 40.00930405724701,
        "longitude": -105.2392134802841,
        "floor": null,
        "description": null,
        "created_date": 1442341374000
    }]
}
```

ATTRIBUTES||
---------:        | -----------
uid<br>*string*   | Unique identifier of the threat
type<br>*string*  | Threat type.  Possible values: `suspicous_person`, `suspicious_object`, `accident`, `road_block`, `road_ice`, `utility`, `weather`, `flood`, `fire`, `wildlife`, `shooting`, `hazardous_material`, `other`
level<br>*string*  | Threat level. Possible values: `low`, `medium`, `high`, `severe`
test<br>*boolean*  | Indicates this was a test submission and should not be shown to your users
latitude<br>*double*  | Latitude of the reported threat
longitude<br>*double*  | Longitude of the reported threat
floor<br>*integer*  | If indoors, floor of the venue<br>*Street level (ground floor) is 0*
address<br>*string*  | Geocoded address of the latitude and longitude
description<br>*string*  | User provided description of the threat
threat_date<br>*timestamp* | Timestamp when the threat occurred.  If not known this date defaults to the reported_date
reported_date<br>*timestamp* | Timestamp when the threat was first reported
media<br>*dictionary*  | List of media objects associated with this threat
