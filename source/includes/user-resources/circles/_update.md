## Update circle

> **Definition**

```text
PUT https://api.fabriq.io/circles
```

> **Sample Request**

```shell
curl -X PUT 'https://api.fabriq.io/circles'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
      "uid": "039d2aa25d4e11e5a0dd38c98601185b",
      "name": "Friends"
     }'
```

> **Sample Response**

```json
{
    "uid": "039d2aa25d4e11e5a0dd38c98601185b",
    "name": "Friends",
    "default": false,
    "photo_url": null
}
```


ARGUMENTS ||
---------:        | -----------
uid<br>**required**, *string* | Circles's uid
name<br>**required**, *string* | New circle name


### Returns
Return the updated circle object.
