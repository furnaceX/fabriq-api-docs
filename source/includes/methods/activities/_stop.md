## End an activity

> Definition

```text
DELETE https://api.fabriq.io/activities/{ACTIVITY_UID}
```

> Sample Request

```shell
curl -X DELETE 'https://api.fabriq.io/activities/804fe823-e230-47aa-b0e9-3131ca6326b1'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -d end_lat=40.01592844038895  \
  -d end_lng=-105.2487217142231
```

> Sample Response

```json
{
    "uid": "191e9aee-58e1-11e5-a0dd-38c98601185b",
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
        "circle_uid": "1939767a-58e1-11e5-a0dd-38c98601185b"
    },{
        "type": "start_activity",
        "circle_uid": "1939767a-58e1-11e5-a0dd-38c98601185b"
    },{
        "type": "end_activity",
        "circle_uid": "1939767a-58e1-11e5-a0dd-38c98601185b"
    }],

    "alerts_triggered": null
}
```

ARGUMENTS ||
---------:        | -----------
end_lat <br>*optional*, *double*  | Latitude where activity ended
end_lng <br>*optional*, *double*  | Longitude where activity ended
disable_alerts <br>*optional*, *boolean*  | If a watch alert was set when the activity was started, the user's contacts will automatically be notified when the activity end.  Set this to true to prevent this notification from being sent.

### Returns
An activity object.
