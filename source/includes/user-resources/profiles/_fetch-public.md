## Retrieve public profile

> **Definition**

```text
GET https://api.fabriq.io/profiles/public
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/profiles/public'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> **Sample Response**

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
    "hair_color": "brown",
    "media": [{
        "uid": "be2aef2302e54b9e9ff9a4cf35c756a2",
        "url": "https://fabriq.io/files/0251/0225/0163/0012C9287B60724FEB0E7669AC49F092F313",
        "content_type": "image/jpeg",
        "size": 45950,
        "latitude": null,
        "longitude": null,
        "floor": null,
        "description": null,
        "created_date": 1442341374150
    }]
}
```

### Returns
The user's pubic profile object.
