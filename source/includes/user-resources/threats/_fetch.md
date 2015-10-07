## Retrieve a threat

> **Definition**

```text
GET https://api.fabriq.io/threats/{THREAT_UID}
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/threats/7ed205f519264529a86014901151dda5'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> **Sample Response**

```json
{
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
}
```

ARGUMENTS  ||
---------: | -----------
threat_uid <br>**required**, *string*  | The UID of the threat to be retrieved


### Returns
A threat object.
