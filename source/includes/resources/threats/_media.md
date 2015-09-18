## Upload media

> Definition

```text
POST https://api.fabriq.io/threats/{THREAT_UID}/media
```

> Sample Request

```shell
curl 'https://api.fabriq.io/threats/7ed205f519264529a86014901151dda5/media'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -F latitude=40.01547488387676  \
  -F longitude=-105.2499169484761  \
  -F file="@/path/to/photo.jpg"
```

> Sample Response

```json
{
    "uid": "fa4c01b994974daf83e4b121a078f428",
    "content_type": "image/jpeg",
    "size": 45950,
    "created_date": 1442341374150,
    "url": "https://fabriq.io/files/0218/0250/0215/00524CF105F2B817EEACE7ACE7AFFC17BA26"
}
```

Upload media files by sending a request of type `multipart/form-data`. The uploaded file should follow
the specifications of RFC 2388 (which defines file transfers for the `multipart/form-data` protocol).

<br>

ARGUMENTS ||
---------:        | -----------
file <br>**required**  | The file to upload.  Currently, only image files are supported.
latitude <br>*optional*  | Latitude where media was captured
longitude <br>*optional*  | Longitude where media was captured
description <br>*optional*  | User provided description of the media


### Returns
This method returns a media object with details of the file uploaded.
