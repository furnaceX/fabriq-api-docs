## Upload media

> **Definition**

```text
POST https://api.fabriq.io/alerts/{ALERT_UID}/media
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/alerts/5c2e0f1b0ce94b7ea75104a2ef022529/media'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -F file="@/path/to/recording.wav"
```

> **Sample Response**

```json
{
    "uid": "e7302afdc5b145b5820a126d96d0885e",
    "content_type": "audio/x-wav",
    "size": 63128,
    "created_date": 1442187162361,
    "url": "https://fabriq.io/files/0007/0044/0012/005598E45DF88488D1E6E8AA7CB9A6CC2E77"
}

{
    "uid": "e7302afdc5b145b5820a126d96d0885e",
    "url": "https://fabriq.io/files/0007/0044/0012/005598E45DF88488D1E6E8AA7CB9A6CC2E77",
    "content_type": "audio/x-wav",
    "size": 63128,
    "latitude": null,
    "longitude": null,
    "floor": null,
    "description": null,
    "created_date": 1442187162361
}
```

Upload media files by sending a request of type `multipart/form-data`.  The uploaded file should follow
the specifications of RFC 2388 (which defines file transfers for the `multipart/form-data` protocol).

<br>

ARGUMENTS ||
---------:        | -----------
file<br>**required**, *file* | The file to upload.  Currently only [WAV](https://en.wikipedia.org/wiki/WAV) and [AMR](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec) audio files are supported.
latitude<br>*optional*, *double*  | Latitude where media was captured
longitude<br>*optional*, *double*  | Longitude where media was captured
floor<br>*optional*, *integer*  | If indoors, floor of the venue<br>*Street level (ground floor) is 0*
description<br>*optional*, *string*  | Description of the media

### Returns
This method returns a media object with details of the file uploaded.
