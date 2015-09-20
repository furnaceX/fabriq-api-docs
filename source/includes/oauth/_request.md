## Request Authorization

> Definition

```text
GET https://api.fabriq.io/oauth/authorize
```

> **Example Request**<br>
> *Line breaks are for formatting only*

```shell
https://api.fabriq.io/oauth/authorize
  ?response_type=code
  &client_id=sb_c21c592ee4454a799b048179cd861144
  &redirect_uri=https%3A%2F%2Fexample.com%2Foauth_callback
  &scope=public_profile,private_profile,contacts,alerts
```


> **Example Approved Response**<br>
> *Redirect with authorization code*

```text
https://example.com/oauth_callback?code=8ts4YQ
```


> **Example Denied Response**<br>
> *Redirect with error message*

```text
https://example.com/oauth_callback?error=access_denied&error_description=User%20denied%20access
```

To obtain a user's authorization, you will need to direct her to FABRIQ's
authorization URL.  The URL's query parameters will include your client application (`client_id`),
the permissions your app requires (`scope`) and the URL the user will be directed to after they grant
or deny permissions to your application (`redirect_uri`).

ARGUMENTS||
---------:        | -----------
response_type<br>**required**, *string*   | Set to `code`
client_id<br>**required**, *string*   | Your application key
redirect_uri<br>**required**, *url*   | After the user approves or denies the authorization request, FABRIQ will redirect to this URL with either an authorization code or an error message appended as a query parameter.  The URL included here must match the one specified in your application details page.
scope<br>**required**, *string*   | Comma separated list of permissions your application requires. Possible values are `public_profile`, `private_profile`, `contacts`, `alerts`, `activities`
