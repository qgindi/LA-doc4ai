# Property `Au.Types.OKey.SleepFinally`

How long to wait (milliseconds) before a "send keys or text" function returns. Default: 10.

```
public int SleepFinally { get; set; }
```

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`int`

Valid values: 0 - 10000 (10 seconds).

#### Remarks

Not used by `Au.clipboard` class functions.

#### Examples

```
opt.key.SleepFinally = 50;
```