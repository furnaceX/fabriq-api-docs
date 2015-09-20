## Access Token

> Definition

```text
POST https://api.fabriq.io/oauth/token
```

> **Example Request**

```shell
curl https://api.fabriq.io/oauth/token  \
  -d grant_type=authorization_code \
  -d client_id=sb_c21c592ee4454a799b048179cd861144 \
  -d redirect_uri=https%3A%2F%2Fexample.com%2Foauth_callback \
  -d code=8ts4YQ
```


> **Example Response**


```json
{
    "access_token": "sb_6328d8d110054601abfb47835fb504d3",
    "refresh_token": "sb_bd0a8cf35209406da1aded79bbcffc36",
    "scope": "alerts private_profile activities public_profile contacts",
    "expires_in": 315357710,
    "token_type": "bearer"
}
```

Once you have an authorization code, you can exchange it for a valid `access_token`.

<br>

ARGUMENTS||
---------:        | -----------
grant_type<br>**required**, *string*   | Set to `authorization_code`
client_id<br>**required**, *string*   | Your application key
redirect_uri<br>**required**, *url*   | This URL must match the one specified in your authorization request
code<br>**required**, *string*   | The authorization code that was included in the redirect URL


<br>

### Response object

<br>

ATTRIBUTES ||
---------:        | -----------
access_token<br>*string*   | Access token with permissions enabled for the requested scopes
refresh_token<br>*string*   | Use the refresh token to update the current access token
scope<br>*string*   | List of scopes authorized by the user
expires_in<br>*integer*   | Number of seconds until this token expires.  
token_type<br>*string*   | Always set to `bearer`

<aside class="warning">
Please note the list of scopes authorized by the user may differ from the set of requested scopes.
</aside>
