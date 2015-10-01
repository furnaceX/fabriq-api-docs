# Authentication


> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/users'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
        "mobile_number": "+12155551111"
      }'
```

Interacting with the API requires a `client_id` (also called an API Key or Application Key).  You can
obtain a `client_id` by signing into the [developer portal](https://developer.fabriq.io) and creating a new application.
A different key is generated for each application you create.

Once obtained, the `client_id` should be included in **every** HTTP request using the custom
X-FABRIQ-CLIENT-ID header.  

For example:


<code style="display:block;text-align:center;margin-top:20px;color:#000;padding:10px;">
X-FABRIQ-CLIENT-ID: 870b1d58a98e4bd0bc489d6ccb3cb66e
</code>

<br>

In addition to the `client_id`, most endpoints require a user `access_token`.  FABRIQ implements the
[OAUTH 2.0](#oauth) standard to enable an application to securely make requests on behalf of a user.

For endpoints that require an OAuth `access_token`, it should be included in the Authorization HTTP header
as a Bearer token.  

For example:

<code style="display:block;text-align:center;margin-top:20px;color:#000;padding:10px;">
Authorization: Bearer fbe54027e4a443d1a2f76adaec1d70d8
</code>


## Sandbox
> **Production Sample Request**

```shell
curl 'https://api.fabriq.io/me' \
  -H 'X-FABRIQ-CLIENT-ID: 870b1d58a98e4bd0bc489d6ccb3cb66e' \
  -H "Authorization: Bearer fbe54027e4a443d1a2f76adaec1d70d8"
```

>  <br/> <br/>


> **Sandbox Sample Request**

```shell
curl 'https://api.fabriq.io/me' \
  -H 'X-FABRIQ-CLIENT-ID: sb_c21c592ee4454a799b048179cd861144' \
  -H "Authorization: Bearer sb_c21c592ee4454a799b048179cd861144"
```

When you create an application in the [developer portal](https://developer.fabriq.io) ,
two client_id's will be generated: a **live-mode** client_id
for production use and a **test-mode** client_id for use in the sandbox environment.  Use the sandbox to test your
code and try out new features.

<aside class="notice">
While the data in the sandbox environment is isolated from the production environment, alerts and notifications are
still sent from this environment.  This means that all users and contacts created in this environment require valid
mobile numbers and email addresses.  Where there are exceptions, they will be noted in the documentation below.
</aside>

All sandbox client_ids and access_tokens are prefixed by **sb_**.

For example:

<code style="display:block;text-align:center;margin-top:20px;color:#000;padding:10px;">
X-FABRIQ-CLIENT-ID: sb_c21c592ee4454a799b048179cd861144
</code>

<br/>

All API requests made using the sandbox `client_id` will be directed to the sandbox environment.  Please note
that access_tokens obtained in the sandbox environment will fail in the production environment.

<br/>

<aside class="warning">
The API is currently in <b><i>beta</i></b>.  In this release, only sandbox client_id's will be generated in
the developer portal.  Live-mode client_id's will be made available once the API is fully released.
</aside>
