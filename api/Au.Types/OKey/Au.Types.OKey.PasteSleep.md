# Property `Au.Types.OKey.PasteSleep`

How long to wait (milliseconds) after pasting (before restoring clipboard data, if need). Default: 100.

```
public int PasteSleep { get; set; }
```

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`int`

Valid values: 0 - 10000 (10 seconds).

#### Remarks

This is the minimal wait time. Actually may wait longer; it depends on how the active window responds.