## Create a user

> **Definition**

```text
POST https://api.fabriq.io/users
```

> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/users'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
        "mobile_number": "+12155551111"
      }'
```

> **Sample Response**

```json
{
    "uid": "f3c84161994841c49d729ff97bd0ead0",
    "username": "f3c84161994841c49d729ff97bd0ead0",
    "email": null,
    "mobile_number": "+12155551112",
    "has_contacts": false,
    "is_verified": false,
    "grants": [
        "panic",
        "geoblast"
    ]
}
```

ARGUMENTS ||
---------:        | -----------
mobile_number <br>**required**, *string*  | User's mobile number ([E.164 format](https://en.wikipedia.org/wiki/E.164))<br>*The user will receive a text message to confirm her mobile number*
email <br>*optional*, *string*  | User's email address (must be valid and unique)<br>*The user will receive an email to confirm her email*
username <br>*optional*, *string*  | User's username (must be valid and available)
first_name <br>*optional*, *string*  | User's first name
last_name <br>*optional*, *string*  | User's last name
login <br>*optional*, *boolean*  | If true, the user will be logged in and the return object will include an access_token

<br/>
<aside class="notice">
Please note that the argument <code>login</code> should be passed in as query parameter in the REST API.
</aside>

<code style="display:block;text-align:center;margin-top:20px;color:#000;padding:10px;">
POST https://api.fabriq.io/users?login=true
</code>

### Returns
A user object.  If the query parameter login is set to true, then the return object will include an
access_token.
