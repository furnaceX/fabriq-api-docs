## Refresh Token

> Definition

```text
POST https://api.fabriq.io/oauth/token
```

> **Example Request**

```shell
curl https://api.fabriq.io/oauth/token  \
  -d grant_type=refresh_token \
  -d client_id=sb_c21c592ee4454a799b048179cd861144 \
  -d refresh_token=sb_6328d8d110054601abfb47835fb504d3
```


> **Example Response**

```json
{
  "access_token": "sb_77f593d1e3cd454c883d47b815a540c0",
  "refresh_token": "sb_913f7fd244174a378476c8c8bcca70dd",
  "scope": "alerts private_profile activities public_profile contacts",
  "expires_in": 315359999,
  "token_type": "bearer"
}
```

The `refresh_token` is used to obtain a new `access_token`.  

<aside class="notice">
Note that when this method is called, the current <code>refresh_token</code> is expired and a new one is issued.
Future calls to refresh the access token must use the most recently issued <code>refresh_token</code>.
</aside>

<br>

ARGUMENTS||
---------:        | -----------
grant_type<br>**required**, *string*   | Set to `refresh_token`
client_id<br>**required**, *string*   | Your application key
refresh_token<br>**required**, *string*   | A valid refresh token


<br>

### Returns
A new `access_token` object.
