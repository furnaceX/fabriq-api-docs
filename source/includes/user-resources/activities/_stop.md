## End an activity

> **Definition**

```text
DELETE https://api.fabriq.io/activities/{ACTIVITY_UID}
```

> **Sample Request**

```shell
curl -X DELETE -G 'https://api.fabriq.io/activities/4ade0a3131ba4e1c942ae40983405391'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -d end_lat=40.01592844038895  \
  -d end_lng=-105.2487217142231
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

    "alerts_triggered": null
}
```

ARGUMENTS ||
---------:        | -----------
end_lat<br>*optional*, *double*  | Latitude where activity ended
end_lng<br>*optional*, *double*  | Longitude where activity ended
disable_alerts<br>*optional*, *boolean*  | If a watch alert was set when the activity was started, the user's contacts will automatically be notified when the activity end.  Set this to true to prevent this notification from being sent.

<br/>
<aside class="notice">
Please note that the arguments are passed in the HTTP DELETE method as query parameters in the REST API.
</aside>

### Returns
An activity object.
