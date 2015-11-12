## Update circle

> **Definition**

```text
PUT https://api.fabriq.io/circles/{CIRCLE_UID}
```

> **Sample Request**

```shell
curl -X PUT 'https://api.fabriq.io/circles/039d2aa25d4e11e5a0dd38c98601185b'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
      "name": "Friends"
     }'
```

> **Sample Response**

```json
{
    "uid": "039d2aa25d4e11e5a0dd38c98601185b",
    "name": "Friends",
    "default": false,
    "photo_url": null,
    "contacts": []
}
```


ARGUMENTS ||
---------:        | -----------
cirlce_uid<br>**required**, *string* | UID of the circle to be updated<br>*URL parameter*
name<br>**required**, *string* | New circle name


### Returns
Return the updated circle object.
