## Add a device

> **Definition**

```text
POST https://api.fabriq.io/devices
```

> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/devices'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
         "name": "Teddy Tag",                   
         "user": "9ff6178e851942cbb5a5ddc71f82588d",                   
         "ble_mac_address": "20:FF:D0:FF:D1:C0",                   
         "capabilities": ["ble"]                   
      }'
```

> **Sample Response**

```json
{
    "uid": "7ce9d0b43d8543b2a53a3990028b4f27",
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
    "hardware_version": null,
    "firmware_version": null,
    "software_version": null,
    "capabilities": ["ble"]
}
```

ARGUMENTS ||
---------:        | -----------
name<br>**required**, *string*  | Name of the device<br>*Unique across all devices owned by the current user*


### Returns
A device object.
