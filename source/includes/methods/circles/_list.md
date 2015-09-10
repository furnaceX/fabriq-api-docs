## List all circles

> Definition

```text
GET https://api.fabriq.io/circles
```

> Sample Request

```shell
curl 'https://api.fabriq.io/circles'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> Sample Response

```json
[{
    "uid": "df2ecdaa-5597-11e5-a0dd-38c98601185b",
    "name": "Default",
    "default": true,
    "photo_url": null
 },
 {
    "uid": "60adf957-4d16-44ef-a271-217f6404b146",
    "name": "Family",
    "default": false,
    "photo_url": null
  }
]
```

### Returns
An array of circles. The array will include at least one circle which is the user's default circle.
