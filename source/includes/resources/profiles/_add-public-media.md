## Add public media

> **Definition**

```text
POST https://api.fabriq.io/profiles/public/media
```

> **Sample Request**

```shell
curl https://api.fabriq.io/profiles/public/media  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"  \
  -F primary_photo=true  \
  -F file="@/path/to/photo.jpg"

```

> **Sample Response**

```json
{
    "uid": "be2aef2302e54b9e9ff9a4cf35c756a2",
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
file <br>**required**, *media file*  | The file to upload.  Currently, only image files are supported
primary_photo <br>*optional*, *boolean*  | Set to true to make this image the user's primary photo
latitude <br>*optional*, *double*  | Latitude where media was captured
longitude <br>*optional*, *double*  | Longitude where media was captured
floor<br>*optional*, *integer*  | If indoors, floor of the venue<br>*Street level (ground floor) is 0*
description <br>*optional* *string*  | User provided description of the media


### Returns
This method returns a [media](#media) object with details of the file uploaded.
