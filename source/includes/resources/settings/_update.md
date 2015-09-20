## Update setting

> Definition

```text
PUT https://api.fabriq.io/settings
```

> Sample Request

```shell
curl -X PUT 'https://api.fabriq.io/settings'  \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'  \
  -H 'Content-Type: application/json'  \
  -d '{                                        
        "panic_delay": 7000
      }'
```

> Sample Response

```json
{
    "panic_delay":7000,
    "panic_silent":true,
    "metric_units":false,
    "alert_panic_message":"PANIC! HELP, I'm in danger!",
    "alert_panic_cancel_message":"This panic alert has been canceled.",
    "alert_activity_start_message":"Hi, letting you know I'm heading out for my workout.",
    "alert_activity_end_message":"Hi, letting you know I'm back from my workout.",
    "alert_activity_timeout_message":"HELP! I went for a workout and should've been back by now!",
    "alert_ping_timeout_message":"HELP! I haven't responded to my security checks!",
    "alert_ping_interval":30000,
    "alert_ping_retry_count":2,
    "alert_ping_timeout":60000
}
```


ARGUMENTS ||
---------:        | -----------
panic_delay <br>*optional*, *integer* |  Milliseconds to wait before a PANIC alert is triggered
panic_silent <br>*optional*, *boolean*  |  Flag to indicate if the device should sound an alarm and flash as strobe by default
metric_units <br>*optional*, *boolean* |  Flag to indicate user's preference in displaying measurements (e.g height and weight)
alert_panic_message <br>*optional*, *string*  |  Message sent when panic is triggered
alert_panic_cancel_message <br>*optional*, *string*  |  Message sent when active alert is canceled
alert_activity_start_message <br>*optional*, *string*  |  Message sent when activity is started
alert_activity_end_message <br>*optional*, *string*  |  Message sent when activity is ended
alert_activity_timeout_message <br>*optional*, *string*  |  Message sent when activity times out
alert_ping_timeout_message <br>*optional*, *string*  |  Message sent when user fails to respond to 'ping_me' after the specified number of retries
alert_ping_interval <br>*optional*, *integer*  |  Milliseconds to wait between successful pings
alert_ping_retry_count <br>*optional*, *integer*  |  Number of times to try a ping before triggering an alert
alert_ping_timeout <br>*optional*, *integer*  |  Milliseconds to wait for a reply from the user


### Returns
Return the updated settings object.
