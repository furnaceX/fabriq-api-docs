## Retrieve a circle

> **Definition**

```text
GET https://api.fabriq.io/circles/{CIRCLE_UID}
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/circles/dea658b2684d11e5922038c98601185b' \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"
```

> **Sample Response**

```json
{
    "uid": "dea658b2684d11e5922038c98601185b",
    "name": "Default",
    "default": true,
    "photo_url": null,
    "contacts": ["2f3771ec87fe11e5ad0738c98601185b"]
}
```

ARGUMENTS  ||
---------: | -----------
circle_uid<br>**required**, *string*  | UID of the circle to be retrieved


### Returns
A circle object.
