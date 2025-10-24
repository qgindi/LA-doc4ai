# Property `Au.Types.OMouse.ClickSpeed`

How long to wait (milliseconds) after sending each mouse button down or up event (2 events for click, 4 for double-click). Default: 20.

```
public int ClickSpeed { get; set; }
```

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`int`

Valid values: 0 - 1000 (1 s).

#### Examples

```
opt.mouse.ClickSpeed = 30;
```