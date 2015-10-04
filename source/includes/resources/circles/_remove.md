## Remove a circle

> **Definition**

```text
DELETE https://api.fabriq.io/circles/{CIRCLE_UID}
```

> **Sample Request**

```shell
curl -X DELETE 'https://api.fabriq.io/circles/df363590684d11e5922038c98601185b' \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"
```

> **Sample Response**

```json
{
    "uid": "df363590684d11e5922038c98601185b"
}
```

ARGUMENTS  ||
---------: | -----------
circle_uid<br>**required**, *string*  | UID of the circle to be removed


<br/>
<aside class="warning">
The user's default circle cannot be removed.
</aside>

<br/>
<aside class="info">
Any contacts associated with this circle will be moved to the user's default circle
before this circle is removed.
</aside>



### Returns
The uid of the circle that was removed.
