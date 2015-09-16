## Retrieve profile

> Definition

```text
GET https://api.fabriq.io/profile
```

> Sample Request

```shell
curl 'https://api.fabriq.io/profile'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> Sample Response

```json
{
    "first_name": "Jane",
    "last_name": "Doe",
    "display_name": "Jane Doe",
    "photo_url": null,
    "birth_date": "1990-01-04",
    "gender": "female",
    "height": 167.64,
    "weight": 54.4311,
    "race": "white",
    "eye_color": "hazel",
    "hair_color": "brown"
}
```

### Returns
The user's profile object.
