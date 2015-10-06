## Upload media

> **Definition**

```text
POST https://api.fabriq.io/contacts/{CONTACT_UID}/media
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/contacts/46b9f6da5da311e5936420c9d07e7899/media'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -F file="@/path/to/photo.jpg"
```

> **Sample Response**

```json
{
    "uid": "53ff178a7bfc473e853a59a680a86a3a",
    "content_type": "image/jpeg",
    "size": 45950,
    "created_date": 1442548487108,
    "url":"https://fabriq.io/files/0057/0183/0164/0118DD3150EDCDB637108536C4188B01F9B5"
}
```

Upload media files by sending a request of type `multipart/form-data`.

<br>

ARGUMENTS ||
---------:        | -----------
file<br>**required**, *file*  | The file to upload.  Currently, only image files are supported.


### Returns
This method returns a [media](#media) object with details of the file uploaded.
