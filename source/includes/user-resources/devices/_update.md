## Update device

> **Definition**

```text
PUT https://api.fabriq.io/devices/{DEVICE_UID}
```

> **Sample Request**

```shell
curl -X PUT 'https://api.fabriq.io/devices/7ce9d0b43d8543b2a53a3990028b4f27'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
      "capabilities": ["ble", "gps", "wifi"]
     }'
```

> **Sample Response**

```json
{
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
    "capabilities": ["ble", "gps", "wifi"]
}
```


ARGUMENTS ||
---------:        | -----------
device_uid<br>**required**, *string* | UID of the device to be updated<br>*URL parameter*
name<br>*optional*, *string*  | Name of the device<br>*Unique across all devices owned by the current user*
type<br>*optional*, *string*  | Device type. Possible values: `phone`, `tablet`, `wearable`, `sensor`, `other`
platform<br>*optional*, *string*   | Platform type. Possible values: `firmware`, `ios`, `os-x`, `watch-os`, `tv-os`, `android`, `linux`, `windows`, `windows-phone`, `unknown`, `other`.<br>*Defaults to `unknown` if not set*
user<br>*optional, *string*  | UID of the user this device is assigned to.
parent<br>*optional*, *string*  | If this device is part of a larger system, then this field references the uid of that larger system.
paried<br>*optional*, *string*  | If this device is currently paired with another device, then this field references the uid of the other device
description<br>*optional*, *string*  | Description of the device
ble_mac_address<br>*optional*, *string*  | [BLE](https://en.wikipedia.org/wiki/Bluetooth_low_energy) MAC address, if this is a bluetooth-enabled device
lan_mac_address<br>*optional*, *string*  | Network MAC address, if this is a network-enabled device
pnp_id<br>*optional*, *string*  | PNP ID of the device
vendor<br>*optional*, *string*  | Vendor of the device
manufacturer<br>*optional*, *string*  | Manufacturer of the device
model_no<br>*optional*, *string*  | Model number of the device
serial_no<br>*optional*, *string*  | Serial number of the device
device_uuid<br>*optional*, *string*  | Manufacturer assigned UUID of the device
hardware_version<br>*optional*, *string*  | Hardware version of the device
firmware_version<br>*optional*, *string*  | Firmware version of the device
software_version<br>*optional*, *string*  | Software version of the device
capabilities<br>*optional*, *array*  | List of features the device supports. Possible values `ble`, `rfid`, `wifi`, `cellular`, `gps`, `camera`, `audio`, `microphone`, `accelerometer`, `gyroscope`

### Returns
Return the updated circle object.
