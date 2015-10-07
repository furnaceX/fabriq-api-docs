## Remove a device

> **Definition**

```text
DELETE https://api.fabriq.io/devices/{DEVICE_UID}
```

> **Sample Request**

```shell
curl -X DELETE 'https://api.fabriq.io/devices/7ce9d0b43d8543b2a53a3990028b4f27' \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H "Authorization: Bearer {ACCESS_TOKEN}"
```

> **Sample Response**

```json
{
    "uid": "7ce9d0b43d8543b2a53a3990028b4f27"
}
```

ARGUMENTS  ||
---------: | -----------
device_uid<br>**required**, *string*  | UID of the device to be removed<br>*URL parameter*


### Returns
The uid of the device that was removed.
