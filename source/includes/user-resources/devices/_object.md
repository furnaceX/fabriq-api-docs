## The device object

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
    "capabilities": ["ble"]
}
```

ATTRIBUTES||
---------:        | -----------
uid<br>*string*   | Unique identifier of the device
type<br>*string*   | Device type. Possible values: `phone`, `tablet`, `wearable`, `sensor`, `other`
platform<br>*string*   | Platform type. Possible values: `firmware`, `ios`, `os-x`, `watch-os`, `tv-os`, `android`, `linux`, `windows`, `windows-phone`, `unknown`, `other`
user<br>*string*  | Uid of the user this device is assigned to.  This may or may not be the current user.<br>*For example, a mom (the current user) could purchase this device (e.g. a BLE tracker) for her child in which case, the uid will be that of her child.*
parent<br>*string*  | If this device is part of a larger system, then this field references the uid of that larger system.<br>*For example, a home security system that has multiple sensors*
paried<br>*string*  | If this device is currently paired with another device, then this field references the uid of the other device
name<br>*string*  | Name of the device
description<br>*string*  | Description of the device
ble_mac_address<br>*string*  | [BLE](https://en.wikipedia.org/wiki/Bluetooth_low_energy) MAC address, if this is a bluetooth-enabled device
lan_mac_address<br>*string*  | Network MAC address, if this is a network-enabled device
pnp_id<br>*string*  | PNP ID of the device
vendor<br>*string*  | Vendor of the device
manufacturer<br>*string*  | Manufacturer of the device
model_no<br>*string*  | Model number of the device
serial_no<br>*string*  | Serial number of the device
device_uuid<br>*string*  | Manufacturer assigned UUID of the device
hardware_version<br>*string*  | Hardware version of the device
firmware_version<br>*string*  | Firmware version of the device
software_version<br>*string*  | Software version of the device
capabilities<br>*array*  | List of features the device supports. Possible values `ble`, `rfid`, `wifi`, `cellular`, `gps`, `camera`, `audio`, `microphone`, `accelerometer`, `gyroscope`
