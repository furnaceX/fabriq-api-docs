## Add a circle

> **Definition**

```text
POST https://api.fabriq.io/circles
```

> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/circles'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
         "name": "Family"                    
      }'
```

> **Sample Response**

```json
{
    "uid": "039d2aa25d4e11e5a0dd38c98601185b",
    "name": "Family",
    "default": false,
    "photo_url": null
}
```

ARGUMENTS ||
---------:        | -----------
name<br>**required**, *string*  | Name of the circle


### Returns
A circle object.
