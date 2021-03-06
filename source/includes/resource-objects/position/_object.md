## The position object

> **Sample Response**

```json
{
    "latitude": 40.0154335191846,
    "longitude": -105.2499519010123,
    "floor": null,
    "altitude": 1606.125526428223,
    "accuracy": 5,
    "altitude_accuracy": 3,
    "heading": 187.03125,
    "speed": 2.410,
    "timestamp": 1401640196770
}
```

ATTRIBUTES ||
---------:| -----------
latitude<br>*double*  | Position latitude
longitude<br>*double*  | Position longitude
floor<br>*integer*  | If indoors, floor of the venue<br>*Street level (ground floor) is 0*
altitude<br>*double*  | Position altitude (meters)
accuracy<br>*double*  | Position accuracy (if available)
altitude_accuracy <br>*double*  | Position altitude accuracy (if available)
heading<br>*double*  | Position heading (degrees clockwise from North)
speed<br>*double*  | Position speed (meters/second)
timestamp<br>*timestamp*  | Timestamp in milliseconds when location was captured
