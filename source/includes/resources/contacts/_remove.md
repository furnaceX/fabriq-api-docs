## Remove a contact

> **Definition**

```text
DELETE https://api.fabriq.io/contacts/{CONTACT_UID}
```

> **Sample Request**

```shell
curl -X DELETE 'https://api.fabriq.io/contacts/38f074edb16241b7a662021425fe7f68' \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"
```

> **Sample Response**

```json
{
    "uid": "38f074edb16241b7a662021425fe7f68"
}
```

ARGUMENTS  ||
---------: | -----------
contact_uid<br>**required**, *string*  | UID of the contact to be removed


### Returns
The uid of the contact that was removed.
