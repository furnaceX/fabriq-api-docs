## Update profile

> Definition

```text
PUT https://api.fabriq.io/profile
```

> Sample Request

```shell
curl -X PUT 'https://api.fabriq.io/profile'        \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -H 'Content-Type: application/json'         \
  -d '{                                        
        "height": 174.2
      }'
```

> Sample Response

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
first_name <br>*optional*  |  -
last_name <br>*optional*  |  -
display_name <br>*optional*  |  -
birth_date <br>*optional*  |  -
gender <br>*optional*  |  -
height <br>*optional*  |  -
weight <br>*optional*  |  -
race <br>*optional*  |  -
eye_color <br>*optional*  |  -
hair_color <br>*optional*  |  -
photo_data <br>*optional*  |  -
photo_content_type <br>*optional*  |  -
photo_size <br>*optional*  |  -


### Returns
Return the updated profile object.
