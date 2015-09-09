## Create a user

> Definition

```text
POST https://api.fabriq.io/users
```

> Sample Request

```shell
curl -X POST 'https://api.fabriq.io/users'   \
  -H 'X-CLIENT-ID: {CLIENT_ID}'              \
  -H 'Content-Type: application/json'        \
  -d '{                                        
        "mobile_number": "2155551111",                    
        "country_code": "US"                 
      }'
```

> Sample Response

```json
{
    "uid": "0001440886991323-a2d5c77b67d7-0001",
    "username": "+12155551111",
    "email": null,
    "mobile_number": "+12155551111",
    "has_contacts": false,
    "is_verified": false,
    "grants":[
        "panic",
        "geoblast",
        "activity_tracking",
        "ping_me",
        "connect_911"
    ]
}
```

ARGUMENTS ||
---------:        | -----------
mobile_number <br>**required**  | User's mobile number
country_code <br>*optional*  | Country were mobile number is registered. Defaults to 'US'
email <br>*optional*  | User's email address (must be valid and unique)
username <br>*optional*  | User's email address (must be valid and available)
first_name <br>*optional*  | User's first name
last_name <br>*optional*  | User's last name
login <br>*optional*  | If true, the user will be logged in and the return object will include an access_token

<br/>
<aside class="notice">
Please note that the argument <code>login</code> should be passed in as query parameter in the REST API.

<code style="display:block;text-align:center;margin-top:20px;color:#000;">
POST https://api.fabriq.io/users?login=true
</code>

</aside>

### Returns
A user object.  If the query parameter login is set to true, then the return object will include an
access_token.
