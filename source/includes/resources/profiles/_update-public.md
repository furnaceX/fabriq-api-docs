## Update public profile

> **Definition**

```text
PUT https://api.fabriq.io/profiles/public
```

> **Sample Request**

```shell
curl -X PUT 'https://api.fabriq.io/profiles/public'        \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -H 'Content-Type: application/json'         \
  -d '{                                        
        "height": 174.2
      }'
```

> **Sample Response**

```json
{
    "first_name": "Jane",
    "last_name": "Doe",
    "display_name": "Jane Doe",
    "photo_url": null,
    "birth_date": "1990-01-04",
    "gender": "female",
    "height": 174.2,
    "weight": 54.4311,
    "race": "white",
    "eye_color": "hazel",
    "hair_color": "brown"
}
```


ARGUMENTS ||
---------:        | -----------
first_name <br>*optional*, *string*  |  User's first name
last_name <br>*optional*, *string*  |  User's last name
birth_date <br>*optional*, *date string*  |  User's birthday formatted as YYYY-MM-DD (e.g. 1980-01-04)
gender <br>*optional*, *string*  | Possible values: `male`, `female`
height <br>*optional*, *double*  |  User's height in centimeters
weight <br>*optional*, *double*  |  User's weight in kilograms
race <br>*optional*, *string*  |  Possible values: `white`, `black`, `hispanic`, `asian`, `native_american`, `pacific_islander`, `other`, `unknown`
eye_color <br>*optional*, *string*  |  Possible values: `brown`, `green`, `blue`, `hazel`
hair_color <br>*optional*, *string*  |  Possible values: `black`, `brown`, `blonde`, `red`, `gray`, `white`, `bald`


### Returns
Return the updated profile object.
