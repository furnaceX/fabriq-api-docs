# OAuth

FABRIQ implements the OAuth 2.0 standard to facilitate user authorization. Similar to Facebook and Twitter’s
authentication flow, the user is first presented with a permission dialog for your application, at which point
the user can either approve the permissions requested, or reject them. Once the user approves, an
authorization_code is sent to your application, which will then be exchanged for an access_token.

The access_token can then be used to make API calls.  

Access tokens currently are long lived and essentially do not expire.  This is will change in a future update of the API.  


## Request Authorization

> **Example Request**

```shell
curl "https://api.fabriq.io/oauth/authorize" \
  -d response_type=code                      \
  -d client_id=${CLIENT_ID}                  \
  -d redirect_uri=${REDIRECT_URI}
```


> **Example Response**

```json
{
    "grants": [
        "panic",
        "geoblast"
    ],
    "uid": "5b4ad9e4-c1c9-4968-84e4-360c61148ec5",
    "first_name": null,
    "last_name": null,
    "photo_url": null,
    "has_contacts": false,
    "is_verified": false,
    "access_token": "test__d9c1f22e-1e41-4696-9643-67f1cc10005d"
}
```

To start the OAuth process, construct the initiation URL which the user will visit in order to grant permission to
your application. The request includes your client application (client_id), and where the user should be redirected to
after they grant or deny permissions to your application (redirect_uri).
