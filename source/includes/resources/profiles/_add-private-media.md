## Upload private media

> **Definition**

```text
POST https://api.fabriq.io/profiles/private/media
```

> **Sample Request**

```shell
curl https://api.fabriq.io/profiles/private/media  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"  \
  -F file="@/path/to/photo.jpg"

```

> **Sample Response**

```json
{
    "uid": "90eeaf15a65c4038b1043cbffab8f7ce",
    "url": "https://fabriq.io/files/0251/0225/0163/0012C9287B60724FEB0E7669AC49F092F313",
    "content_type": "image/jpeg",
    "size": 45950,
    "latitude": null,
    "longitude": null,
    "floor": null,
    "description": null,
    "created_date": 1442341374150
}
```

Upload media files by sending a request of type `multipart/form-data`.


<br>

ARGUMENTS ||
---------:        | -----------
file<br>**required**, *media file*  | The file to upload.  Currently, only image files are supported
latitude<br>*optional*, *double*  | Latitude where media was captured
longitude<br>*optional*, *double*  | Longitude where media was captured
floor<br>*optional*, *integer*  | If indoors, floor of the venue<br>*Street level (ground floor) is 0*
description<br>*optional* *string*  | User provided description of the media


### Returns
This method returns a [media](#media) object with details of the file uploaded.
