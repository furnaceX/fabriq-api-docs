## The settings object

> **Sample Response**

```json
{
    "panic_delay": 5000,
    "panic_silent": true,
    "pin_ok": "1234",
    "pin_duress": "5678",
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

ATTRIBUTES||
---------:        | -----------
panic_delay<br>*integer*   | [UI] Time in milliseconds to wait before the PANIC alert is triggered.  The user should be able to cancel the alert during this window.
panic_silent<br>*boolean*  | [UI] Flag to indicate a PANIC alert should be triggered silently.
pin_ok<br>*string*  | PIN used to cancel an alert.  This PIN will cancel the alert and send a notification to the user's contacts
pin_duress<br>*string*  | In a situation where a user is forced to turn off the alert, this PIN is used to disable the  UI but keep the alert active
metric_units<br>*boolean*  | [UI] User preference to view/update his or her profile data
alert_panic_message<br>*string*  | Message sent when panic is triggered
alert_panic_cancel_message<br>*string*  | Message sent when active alert is canceled
alert_activity_start_message<br>*string*  | Message sent when activity is started
alert_activity_end_message<br>*string*  | Message sent when activity is ended
alert_activity_timeout_message<br>*string*  | Message sent when activity times out
alert_ping_timeout_message<br>*string*  | Message sent when user fails to respond to 'ping_me' after the specified number of retries
alert_ping_interval<br>*integer*  | Milliseconds between sending a `ping` message to the user
alert_ping_timeout<br>*integer*  | Milliseconds to wait for a user to respond to a `ping`
alert_ping_retry_count<br>*integer*  | Number of times to try a `ping` after a timeout before triggering an alert
