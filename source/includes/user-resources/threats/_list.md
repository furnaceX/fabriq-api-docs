## List nearby threats

> **Definition**

```text
GET https://api.fabriq.io/threats
```

> **Sample Request**

```shell
curl -G 'https://api.fabriq.io/threats'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -d latitude=40.00930405724701  \
  -d longitude=-105.2392134802841  \
  -d radius=3218 \
  -d levels=medium \
  -d types=accident \
  -d types=wildlife
```

> **Sample Response**

```json
[{
    "uid": "7ed205f519264529a86014901151dda5",
    "type": "wildlife",
    "level": "medium",
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
}]
```

ARGUMENTS  ||
---------: | -----------
latitude <br>**required**, *double*  | Latitude of current position
longitude <br>**required**, *double*  | Longitude of current position
radius <br>**required**, *double*  | Radius (in meters) of reported threats
max_age <br>*optional*, *integer*  | Only return threats that have been reported less than this time ago (in ms)
types <br>*optional*, *list*  | Return threats that only match the listed types. Possible values: `suspicous_person`, `suspicious_object`, `accident`, `road_block`, `road_ice`, `utility`, `weather`, `flood`, `fire`, `wildlife`, `shooting`, `hazardous_material`, `other`
levels <br>*optional*, *list*  | Return threats that only match the listed levels. Possible values: `low`, `medium`, `high`, `severe`


### Returns
A list of threat objects that match the specified criteria.
