## Public profile

> **Sample Response**

```json
{
    "first_name": "Jane",
    "last_name": "Doe",
    "display_name": "Jane Doe",
    "photo_url": "https://fabriq.io/files/0097/0123/0143/0021CD5022F19414CA70274A428672E296D6",
    "birth_date": "1990-01-04",
    "gender": "female",
    "height": 167.64,
    "weight": 54.4311,
    "race": "white",
    "eye_color": "hazel",
    "hair_color": "brown",
    "media": [{
        "uid": "be2aef2302e54b9e9ff9a4cf35c756a2",
        "url": "https://fabriq.io/files/0251/0225/0163/0012C9287B60724FEB0E7669AC49F092F313",
        "content_type": "image/jpeg",
        "size": 45950,
        "latitude": null,
        "longitude": null,
        "floor": null,
        "description": null,
        "created_date": 1442341374150
    }]
}
```

ATTRIBUTES||
---------:        | -----------
first_name<br>*string*   | User's first name
last_name<br>*string*  | User's last name
display_name<br>*string*  | User's full name
photo_url<br>*url*  | Link to user's photo
birth_date<br>*date string*  |  User's birthday formatted as YYYY-MM-DD (e.g. 1980-01-04)
gender<br>*string*  | User's gender. Values: `male`, `female`
height<br>*double*  | User's height in centimeters
weight<br>*double*  | User's weight in kilograms
race<br>*string*  | User's ethnicity. Values: `white`, `black`, `hispanic`, `asian`, `native_american`, `pacific_islander`, `other`, `unknown`
eye_color<br>*string*  | User's eye color. Values: `brown`, `green`, `blue`, `hazel`
hair_color<br>*string*  | User's hair color. Values: `black`, `brown`, `blonde`, `red`, `gray`, `white`, `bald`
media<br>*array*  | List of public media objects associated with this profile
