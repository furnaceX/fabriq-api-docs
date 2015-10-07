## Add a logo

> **Definition**

```text
POST https://api.fabriq.io/circles/{CIRCLE_UID}/media
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/circles/039d2aa25d4e11e5a0dd38c98601185b/media'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
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

Upload a logo or photo to represent this circle.

<br>

ARGUMENTS ||
---------:        | -----------
file<br>**required**, *file*  | The file to upload.  Currently, only image files are supported.


### Returns
This method returns a [media](#media) object with details of the file uploaded.
