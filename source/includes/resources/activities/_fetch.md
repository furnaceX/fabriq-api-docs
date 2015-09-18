## Retrieve an activity

> Definition

```text
GET https://api.fabriq.io/activities/{ACTIVITY_UID}
```

> Sample Request

```shell
curl 'https://api.fabriq.io/activities/4ade0a3131ba4e1c942ae40983405391'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> Sample Response

```json
{
    "uid": "4ade0a3131ba4e1c942ae40983405391",
    "type": "run",
    "name": "07/01/2015 06:42 AM",

    "start_lat": 40.00930405724701,
    "start_lng": -105.2392134802841,
    "start_address": "1279 Harrison Ct, Boulder, CO 80303, USA",

    "end_lat": 40.01554089136423,
    "end_lng": -105.2499387414243,
    "end_address": "1654 33rd St, Boulder, CO 80303, USA",

    "dest_lat": null,
    "dest_lng": null,
    "dest_address": null,

    "start_date": 1435754562000,
    "end_date": 1435755238000,

    "elapsed_time": 676000,
    "total_distance": 1897.0087033661473,
    "average_speed": 2.900624928694415,

    "alert_settings": [{
        "type": "timeout",
        "timeout": 2400000,
        "circle_uid": "039d2aa25d4e11e5a0dd38c98601185b"
    },{
        "type": "start_activity",
        "circle_uid": "039d2aa25d4e11e5a0dd38c98601185b"
    },{
        "type": "end_activity",
        "circle_uid": "039d2aa25d4e11e5a0dd38c98601185b"
    }],

    "alerts_triggered": null
}
```

ARGUMENTS  ||
---------: | -----------
activity_uid<br>**required**, *string*  | The UID of the activity to be retrieved


### Returns
An activity object if a valid UID was provided.
