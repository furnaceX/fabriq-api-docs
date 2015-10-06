## Remove a threat

> **Definition**

```text
DELETE https://api.fabriq.io/threats/{THREAT_UID}
```

> **Sample Request**

```shell
curl -X DELETE 'https://api.fabriq.io/threats/775a91b7390d4108ba650003143f8487'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  
```

> **Sample Response**

```json
{
    "uid": "775a91b7390d4108ba650003143f8487"
}
```

ARGUMENTS ||
---------:        | -----------
threat_uid <br>**required**, *string*  | The UID of the threat to be removed


### Returns
An object with the deleted status set.
