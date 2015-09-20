# OAuth

FABRIQ implements the OAuth 2.0 standard to facilitate user authorization. Similar to Facebook and Twitter’s
authentication flow, the user is first presented with a permission dialog for your application, at which point
the user can either approve the permissions requested, or reject them. If the user approves the authorization request,
an authorization_code is sent to your application, which will then be exchanged for an access_token.

The access_token can then be used to make API calls.  

Access tokens currently are long lived and essentially do not expire.  This will change in a future update of the API.  
