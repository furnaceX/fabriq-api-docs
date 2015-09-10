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
         "name": "Family"                    
      }'
```

> Sample Response

```json
{
    "uid": "60adf957-4d16-44ef-a271-217f6404b146",
    "name": "Family",
    "default": false,
    "photo_url": null
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
