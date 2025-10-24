# Method `Au.More.RecordingUtil.MouseToString`

Converts multiple recorded mouse movements to string for `Au.mouse.moveBy`.

```
public static string MouseToString(IEnumerable<uint> recorded, bool withSleepTimes)
```

##### Parameters

- *recorded*  (`IEnumerable<uint>`):
    List of x y distances from previous. The first distance is from mouse position before the first movement; at run time it will be distance from `Au.mouse.lastXY`. To create `uint` value from distance *dx* *dy* use `Au.More.Math2.MakeLparam` and cast to `uint`.
- *withSleepTimes*  (`bool`):
    *recorded* also contains sleep times (milliseconds) alternating with distances. It must start with a sleep time. Example: `{time1, dist1, time2, dist2}`. Another example: `{time1, dist1, time2, dist2, time3}`. This is invalid: `{dist1, time1, dist2, time2}`.

##### Returns

`string`