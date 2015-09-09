## Update setting

> Definition

```text
PUT https://api.fabriq.io/settings
```

> Sample Request

```shell
curl -X PUT 'https://api.fabriq.io/settings'        \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'   \
  -H 'Content-Type: application/json'         \
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
    "alert_ping_me_timeout_message":"HELP! I haven't responded to my security checks!",
    "alert_ping_me_interval":30000,
    "alert_ping_me_retry_count":2,
    "alert_ping_me_timeout":60000
}
```


ARGUMENTS ||
---------:        | -----------
panic_delay <br>*optional*  |  -
panic_silent <br>*optional*  |  -
metric_units <br>*optional*  |  -
alert_panic_message <br>*optional*  |  -
alert_panic_cancel_message <br>*optional*  |  -
alert_activity_start_message <br>*optional*  |  -
alert_activity_end_message <br>*optional*  |  -
alert_activity_timeout_message <br>*optional*  |  -
alert_ping_me_timeout_message <br>*optional*  |  -
alert_ping_me_interval <br>*optional*  |  -
alert_ping_me_retry_count <br>*optional*  |  -
alert_ping_me_timeout <br>*optional*  |  -


### Returns
Return the updated settings object.
