## Upload media

> Definition

```text
POST https://api.fabriq.io/activities/{ACTIVITY_UID}/media
```

> Sample Request

```shell
curl 'https://api.fabriq.io/activities/ff77462fd128430b94c083b6f88f1cb9/media'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -F file="@/path/to/photo.jpg;type=image/jpeg"
```

> Sample Response

```json
{
    "uid": "e7302afdc5b145b5820a126d96d0885e",
    "content_type": "image/jpeg",
    "size": 63128,
    "created_date": 1442187162361,
    "url": "https://fabriq.io/files/0007/0044/0012/005598E45DF88488D1E6E8AA7CB9A6CC2E77"
}
```

Upload media files by sending a request of type `multipart/form-data`.  The request should contain the file and
specify its content-type.

<br>

ARGUMENTS ||
---------:        | -----------
file <br>**required**  | The file to upload. The file should follow the specifications of RFC 2388 (which defines file transfers for the `multipart/form-data` protocol).
content_type <br>**required**  | Content-Type of the uploaded file. Currently, only image files are supported.
latitude <br>*optional*  | Latitude where media was captured
longitude <br>*optional*  | Longitude where media was captured
description <br>*optional*  | User provided description of the media


### Returns
This method returns a media object with details of the file uploaded.
