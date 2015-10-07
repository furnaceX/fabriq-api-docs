## Remove media

> **Definition**

```text
DELETE https://api.fabriq.io/threats/{THREAT_UID}/media/{MEDIA_UID}
```

> **Sample Request**

```shell
curl -X DELETE 'https://api.fabriq.io/threats/7ed205f519264529a86014901151dda5/media/fa4c01b994974daf83e4b121a078f428' \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"
```

> **Sample Response**

```json
{
    "uid": "fa4c01b994974daf83e4b121a078f428"
}
```

ARGUMENTS  ||
---------: | -----------
media_uid<br>**required**, *string*  | UID of the media object to be removed


### Returns
The uid of the media object that was removed.
