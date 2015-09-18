## Upload media

> Definition

```text
POST https://api.fabriq.io/alerts/{ALERT_UID}/media
```

> Sample Request

```shell
curl -X POST 'https://api.fabriq.io/alerts/8d3dd9ed-146e-4526-a69b-d06c7d12cbf9/media'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -H 'Content-Type: application/json'         \
  -d '{                                        
        "content_type": "audio/wav",
        "data": "aGVsbG8gd29ybGQ=",
      }'
```

> Sample Response

```text
{
    "uid": "e7302afdc5b145b5820a126d96d0885e",
    "content_type": "audio/wav",
    "size": 63128,
    "created_date": 1442187162361,
    "url": "https://fabriq.io/files/0007/0044/0012/005598E45DF88488D1E6E8AA7CB9A6CC2E77"
}
```

ARGUMENTS ||
---------:        | -----------
content_type <br>**required**  | Media contenty type. Currently, only `audio/wav` and `audio/AMR` types are supported.
data <br>**required**  | The media data <b>base64 encoded</b>.
size <br>*optional*  | The size of the media file.  NOTE: This is not the size of the base64 encoded string but the size of the original media file.


### Returns
This method returns a media object with details of the upload.
