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

To obtain a user's authorization to access her account, you will need to direct her to FABRIQ's
authorization URL.  The URL's query parameters will include your client application (client_id),
the permissions your app requires (scope) and the URL the user will be directed to after they grant
or deny permissions to your application (redirect_uri).

ARGUMENTS||
---------:        | -----------
grant_type<br>**required**, *string*   | Set to `authorization_code`
client_id<br>**required**, *string*   | Your application key
redirect_uri<br>**required**, *url*   | This URL must match the one specified in your authorization request
code<br>**required**, *string*   | The authorization code that was included in the redirect URL


### Response object

ATTRIBUTES ||
---------:        | -----------
access_token<br>*string*   | Access token with permissions enabled for the requested scopes
expires_in<br>*integer*   | Number of seconds until this token expires.  
token_type<br>*string*   | Alwasy set to `bearer`
