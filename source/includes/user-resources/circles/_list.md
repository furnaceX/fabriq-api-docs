## List all circles

> **Definition**

```text
GET https://api.fabriq.io/circles
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/circles'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> **Sample Response**

```json
[{
    "uid": "45778d285da311e5936420c9d07e7899",
    "name": "Default",
    "default": true,
    "photo_url": null,
    "contacts": ["2f3771ec87fe11e5ad0738c98601185b"]
},
{
    "uid": "039d2aa25d4e11e5a0dd38c98601185b",
    "name": "Family",
    "default": false,
    "photo_url": null,
    "contacts": []
 }]
```

### Returns
An array of circles. The array will include at least one circle which is the user's default circle.
