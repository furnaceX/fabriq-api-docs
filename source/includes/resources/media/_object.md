## The media object

> **Sample Response**

```json
{
    "uid": "fa4c01b994974daf83e4b121a078f428",
    "url": "https://fabriq.io/files/0218/0250/0215/00524CF105F2B817EEACE7ACE7AFFC17BA26",
    "content_type": "image/jpeg",
    "size": 45950,
    "latitude": null,
    "longitude": null,
    "floor": null,
    "description": null,
    "created_date": 1442341374150
}
```

ATTRIBUTES ||
---------:| -----------
uid<br>*string*  | Unique identifier of the media object
url<br>*url*  | URL to access the uploaded file.  Depending on the context of the upload this file may or may not be publicly accessible.
content_type<br>*string*  | The content-type of the uploaded file as determined by FABRIQ
size<br>*integer*  | Size in bytes of the uploaded file
latitude<br>*double*  | Latitude where media object was captured
longitude<br>*double*  | Longitude where media object was captured
floor<br>*integer*  | If indoors, floor of the venue<br>*Street level (ground floor) is 0*
description<br>*string*  | Description of the media object
created_date<br>*timestamp*  | Date file was uploaded
