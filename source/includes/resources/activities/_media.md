## Upload media

> **Definition**

```text
POST https://api.fabriq.io/activities/{ACTIVITY_UID}/media
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/activities/ff77462fd128430b94c083b6f88f1cb9/media'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -F latitude=40.01547488387676  \
  -F longitude=-105.2499169484761  \
  -F file="@/path/to/photo.jpg"
```

> **Sample Response**

```json
{
  "uid": "990610ab5b2d437cab3205523dcb83a5",
  "content_type": "image/jpeg",
  "size": 45950,
  "created_date": 1442289154770,
  "url": "https://fabriq.io/files/0200/0220/0224/024983F11F0912BA570C8D6CB1E345E770C0"
}
```

Upload media files by sending a request of type `multipart/form-data`.

<br>

ARGUMENTS ||
---------:        | -----------
file<br>**required**, *file*  | The file to upload.  Currently, only image files are supported.
latitude<br>*optional*, *double*  | Latitude where media was captured
longitude<br>*optional*, *double*  | Longitude where media was captured
description<br>*optional*, *string*  | User provided description of the media


### Returns
This method returns a [media](#media) object with details of the file uploaded.
