## List all devices

> **Definition**

```text
GET https://api.fabriq.io/devices
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/devices'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> **Sample Response**

```json
[{
    "uid": "7ce9d0b43d8543b2a53a3990028b4f27",
    "type": "wearable",
    "platform": "firmware",
    "user": "9ff6178e851942cbb5a5ddc71f82588d",
    "parent": null,
    "paired": null,
    "name": "Teddy Tag",
    "description": null,
    "ble_mac_address": "20:FF:D0:FF:D1:C0",
    "lan_mac_address": null,
    "pnp_id": null,
    "vendor": null,
    "manufacturer": null,
    "model_no": null,
    "serial_no": null,
    "device_uuid": null,
    "hardware_version": null,
    "firmware_version": null,
    "software_version": null,
    "capabilities": ["ble"]
}]
```

### Returns
An array of devices.
