## Retrieve public profile

> Definition

```text
GET https://api.fabriq.io/profiles/public
```

> Sample Request

```shell
curl 'https://api.fabriq.io/profiles/public'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> Sample Response

```json
{
    "first_name": "Jane",
    "last_name": "Doe",
    "display_name": "Jane Doe",
    "photo_url": "https://fabriq.io/files/0097/0123/0143/0021CD5022F19414CA70274A428672E296D6",
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
The user's pubic profile object.
