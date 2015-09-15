## Upload media

> Definition

```text
POST https://api.fabriq.io/alerts/{ALERT_UID}/media
```

> Sample Request

```shell
curl 'https://api.fabriq.io/alerts/ff77462fd128430b94c083b6f88f1cb9/media'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -F file="@/path/to/recording.wav"
```

> Sample Response

```json
{
    "uid": "e7302afdc5b145b5820a126d96d0885e",
    "content_type": "audio/x-wav",
    "size": 63128,
    "created_date": 1442187162361,
    "url": "https://fabriq.io/files/0007/0044/0012/005598E45DF88488D1E6E8AA7CB9A6CC2E77"
}
```

Upload media files by sending a request of type `multipart/form-data`.  The uploaded file should follow
the specifications of RFC 2388 (which defines file transfers for the `multipart/form-data` protocol).

<br>

ARGUMENTS ||
---------:        | -----------
file <br>**required**  | The file to upload.  Currently only [WAV](https://en.wikipedia.org/wiki/WAV) and [AMR](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec) audio files are supported.

### Returns
This method returns a media object with details of the file uploaded.
