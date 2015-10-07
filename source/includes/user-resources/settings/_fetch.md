## Retrieve settings

> **Definition**

```text
GET https://api.fabriq.io/settings
```

> **Sample Request**

```shell
curl 'https://api.fabriq.io/settings'  \
  -H 'X-FABRIQ-CLIENT-ID: {CLIENT_ID}' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}'
```

> **Sample Response**

```json
{
    "panic_delay": 5000,
    "panic_silent": true,
    "metric_units": false,
    "alert_panic_message": "PANIC! HELP, I'm in danger!",
    "alert_panic_cancel_message": "This panic alert has been canceled.",
    "alert_activity_start_message": "Hi, letting you know I'm heading out for my workout.",
    "alert_activity_end_message": "Hi, letting you know I'm back from my workout.",
    "alert_activity_timeout_message": "HELP! I went for a workout and should've been back by now!",
    "alert_ping_timeout_message": "HELP! I haven't responded to my safety check-in message!",
    "alert_ping_interval": 30000,
    "alert_ping_retry_count": 2,
    "alert_ping_timeout": 60000
}
```

### Returns
The user's settings object.
