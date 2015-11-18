## Retrieve current user

> **Definition**

```text
GET https://api.fabriq.io/me
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/me' \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"
```

> **Sample Response**

```json
{
    "uid": "9ff6178e851942cbb5a5ddc71f82588d",
    "username": "johndoe1234",
    "email": "test@example.com",
    "mobile_number": "+12155551111",
    "has_contacts": true,
    "is_verified": true,
    "grants":[
        "panic",
        "geoblast",
        "breadcrumbs",
        "ping",
        "911"
    ]
}
```

### Returns
Return the current user associated with the access_token.
