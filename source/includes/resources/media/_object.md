## The media object

> **Sample Response**

```json
{
    "uid": "fa4c01b994974daf83e4b121a078f428",
    "content_type": "image/jpeg",
    "size": 45950,
    "created_date": 1442341374150,
    "url": "https://fabriq.io/files/0218/0250/0215/00524CF105F2B817EEACE7ACE7AFFC17BA26"
}
```

ATTRIBUTES ||
---------:| -----------
uid<br>*string*  | Unique identifier of the media object
content_type<br>*string*  | The content-type of the uploaded file as determined by FABRIQ
size<br>*integer*  | Size in bytes of the uploaded file
created_date<br>*timestamp*  | Date file was uploaded
url<br>*url*  | URL to access the uploaded file.  Depending on the context of the upload this file may or may not be publicly accessible.
