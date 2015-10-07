## Remove private media

> **Definition**

```text
DELETE https://api.fabriq.io/profiles/private/media/{MEDIA_UID}
```

> **Sample Request**

```shell
curl -X DELETE 'https://api.fabriq.io/profiles/private/media/90eeaf15a65c4038b1043cbffab8f7ce' \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"
```

> **Sample Response**

```json
{
    "uid": "90eeaf15a65c4038b1043cbffab8f7ce"
}
```

ARGUMENTS  ||
---------: | -----------
media_uid<br>**required**, *string*  | UID of the private media object to be removed


### Returns
The uid of the media object that was removed.
