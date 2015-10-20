## The activity object

> **Sample Response**

```json
{
    "uid": "4ade0a3131ba4e1c942ae40983405391",
    "type": "run",
    "name": "07/01/2015 06:42 AM",

    "start_lat": 40.00930405724701,
    "start_lng": -105.2392134802841,
    "start_floor": null,
    "start_address": "1279 Harrison Ct, Boulder, CO 80303, USA",

    "end_lat": 40.01554089136423,
    "end_lng": -105.2499387414243,
    "end_floor": null,
    "end_address": "1654 33rd St, Boulder, CO 80303, USA",

    "dest_lat": null,
    "dest_lng": null,
    "dest_floor": null,
    "dest_address": null,

    "start_date": 1435754562000,
    "end_date": 1435755238000,

    "elapsed_time": 676000,
    "total_distance": 1897.0087033661473,
    "average_speed": 2.900624928694415,

    "alert_settings": [{
        "type": "timeout",
        "timeout": 2400000,
        "circles": [ "039d2aa25d4e11e5a0dd38c98601185b" ]
    },{
        "type": "start_activity",
        "circles": [ "039d2aa25d4e11e5a0dd38c98601185b" ]
    },{
        "type": "end_activity",
        "circles": [ "039d2aa25d4e11e5a0dd38c98601185b" ]
    }],

    "alerts_triggered": [ "451bc6c0-8231-44dd-8168-d722b86f04f5" ]
}
```

ATTRIBUTES||
---------:        | -----------
uid<br>*string*   | Unique identifier of the activity
type<br>*string*  | Activity type. Values: `fitness`, `social`, `dating`, `travel`, `shopping`, `work`, `other`<br>*Additional activities will be added in future updates.*
start_lat<br>*double*  | Latitude where activity started
start_lng<br>*double*  | Longitude where activity started
start_address<br>*string*  | Geocoded start address
dest_lat<br>*double*  | Destination latitude
dest_lng<br>*double*  | Destination longitude
dest_address<br>*string*  | Geocoded destination address
end_lat<br>*double*  |  Latitude where activity ended
end_lng<br>*double*  | Longitude where activity ended
end_address<br>*string*  | Geocoded end address
start_date<br>*timestamp*  | Timestamp (UTC) when activity started
end_date<br>*timestamp*  | Timestamp (UTC) when activity ended
elapsed_time<br>*integer*  | Duration of activity (ms)
total_distance<br>*double*  | Total distance traveled (meters)
average_speed<br>*double*  | Calculated average speed (meters/second)
alert_settings<br>*list*  | List of [alert_setting](#the-alert_setting-object) objects
alerts_triggered<br>*list*  | List of `alert_uid` triggered for this activity. Returns `null` if no alerts were triggered.


### The alert_setting object

ATTRIBUTES||
---------:        | -----------
type <br>*string*  | Alert type. Values: `start_activity`, `end_activity`, `timeout`, `ping`
circles <br>*list*  | The list of `circle_uid` that will notified if this alert is triggered
timeout <br>*integer*  | [`timeout`, `ping`] Time (ms) to elapse before alert is triggered
interval <br>*integer*  | [`ping`] Time (ms) between ping requests
retry_count <br>*integer*  | [`ping`] Number of times to try a timed out ping before an alert is triggered
