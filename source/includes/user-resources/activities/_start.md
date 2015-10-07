## Start an activity

> **Definition**

```text
POST https://api.fabriq.io/activities
```

> **Sample Request**

```shell
curl -X POST 'https://api.fabriq.io/activities'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
         "type": "run",                    
         "start_lat": 40.00930405724701,                    
         "start_lng": -105.2392134802841,
         "dest_address": "1617 Pearl St, Boulder, CO 80302",
         "alert_watch": true,                    
         "alert_timeout": 900000,                    
         "circles": [ "039d2aa25d4e11e5a0dd38c98601185b" ]
      }'
```

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

    "end_lat": null,
    "end_lng": null,
    "end_floor": null,
    "end_address": null,

    "dest_lat": 40.01554089136423,
    "dest_lng": -105.2499387414243,
    "dest_floor": null,
    "dest_address": "1654 33rd St, Boulder, CO 80303, USA",

    "start_date": 1435754562000,
    "end_date": null,

    "elapsed_time": null,
    "total_distance": null,
    "average_speed": null,

    "alert_settings": [{
        "type": "timeout",
        "timeout": 2400000,
        "circles": [ "039d2aa25d4e11e5a0dd38c98601185b" ]
    },{
        "type": "start_activity",
        "circles": [ "039d2aa25d4e11e5a0dd38c98601185b" ]
    }],

    "alerts_triggered": null
}
```

ARGUMENTS ||
---------:        | -----------
type<br>**required**, *string* | Activity type. Values: `run`, `walk`, `bike`, `social`, `travel`, `other`<br>*Additional activities will be added in future updates.*
start_lat<br>**required**, *double* | Latitude where activity started
start_lng<br>**required**, *double* | Longitude where activity started
name<br>*optional*, *string*| Name of this activity.  Defaults to local date and time.
dest_address<br>*optional*, *string*  | Destination address associated with activity
alert_watch<br>*optional*, *boolean*  | Flag to request user's contacts to watch him or her.  Each contact will receive a message when the activity starts (and optionally when the activity stops) with a link to watch the user in real time.
alert_timeout<br>*optional*, *integer*  | Number of milliseconds that the user expects the activity to last.  If the activity is not ended before this time, an alert will be triggered.  This timeout can be extended if the activity takes longer than the user initially anticipated.
alert_ping_interval<br>*optional*, *integer*  | This enables the [ping](#ping-alert) feature and sets the number of milliseconds between ping requests.
alert_ping_timeout<br>*optional*, *integer*  | Number of milliseconds to wait for a user reply before the ping is flagged as an alert.
alert_ping_retry_count<br>*optional*, *integer*  | Number of times to try a timed out ping before an alert is triggered.
circles<br>*optional*, *list*  | Array of `circle_uid`'s which will be messaged for the specified alert settings. This is required if any of the alert options are set.


### Returns
An activity object.
