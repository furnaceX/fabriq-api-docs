## Add a circle

> Definition

```text
POST https://api.fabriq.io/circles
```

> Sample Request

```shell
curl -X POST 'https://api.fabriq.io/circles'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
         "name": "Friends"                    
      }'
```

> Sample Response

```json
{
    "uid": "761d4f1a-a121-40f8-a8d3-2993ba5861d9",
    "first_name": "Jane",
    "last_name": "Doe",
    "display_name": "Jane doe",
    "photo_url": null,
    "email": " jane@example.com",
    "mobile_number": "+12125551313",
    "email_alert": false,
    "sms_alert": false,
    "push_alert": false,
    "email_verified": false,
    "mobile_verified": false,
    "circles":[{
        "uid": "d4826772-542f-11e5-9364-20c9d07e7899",
        "photo_url": null,
        "display_name": "Default"
    }]
}
```

ARGUMENTS ||
---------:        | -----------
name <br>**required**  | Name of the circle
photo_data <br>*optional*  | Circle photo base64 encoded
photo_content_type <br>*optional*  | Photo content type. (Required if photo_data is specified)
photo_size <br>*optional*  | Size of the photo.


### Returns
A circle object.
