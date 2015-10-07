## Remove public media

> **Definition**

```text
DELETE https://api.fabriq.io/profiles/public/media/{MEDIA_UID}
```

> **Sample Request**

```shell
curl -X DELETE 'https://api.fabriq.io/profiles/public/media/be2aef2302e54b9e9ff9a4cf35c756a2' \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"
```

> **Sample Response**

```json
{
    "uid": "be2aef2302e54b9e9ff9a4cf35c756a2"
}
```

ARGUMENTS  ||
---------: | -----------
media_uid<br>**required**, *string*  | UID of the public media object to be removed


### Returns
The uid of the media object that was removed.
