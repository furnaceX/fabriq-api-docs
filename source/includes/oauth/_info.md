# OAuth

FABRIQ implements OAuth 2.0 to enable a third-party application to access a user's account on her behalf.  The
application first directs the user to a FABRIQ permission page where she can either approve or deny the
authorization request. If the user approves the request, an `authorization_code` is sent to the application,
which will then be exchanged for an `access_token`.

The `access_token` can then be used to make API calls.  

Access tokens currently are long lived by design so that a PANIC alert can be triggered at any time.  Future updates
are likely to change the expiration length so to avoid any disruption in connectivity it's best to refresh the token
at least once a month.
