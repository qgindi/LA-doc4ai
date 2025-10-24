# Property `Au.wnd.ClientRect`

Gets client area rectangle (width and height).

```
public RECT ClientRect { get; }
```

##### Property Value

`Au.Types.RECT`

#### Remarks

The left and top fields are always 0. Calls `Au.wnd.GetClientRect`. Returns `default(RECT)` if fails (eg window closed).