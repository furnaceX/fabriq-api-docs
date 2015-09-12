## Retrieve current user

> Definition

```text
GET https://api.fabriq.io/me
```

> Sample Request

```shell
curl 'https://api.fabriq.io/me'               \
  -H "Authorization: Bearer {ACCESS_TOKEN}"
```

> Sample Response

```json
{
    "uid": "0001440886991323-a2d5c77b67d7-0001",
    "username": "+12155551111",
    "email": null,
    "mobile_number": "+12155551111",
    "has_contacts": false,
    "is_verified": false,
    "grants": [
        "panic",
        "geoblast",
        "activity_tracking",
        "ping_me",
        "connect_911"
    ]
}
```

### Returns
Return the current user associated with the access_token.
