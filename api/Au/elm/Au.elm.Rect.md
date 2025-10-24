# Property `Au.elm.Rect`

Gets location of this UI element in screen.

```
public RECT Rect { get; }
```

##### Property Value

`Au.Types.RECT`

Empty rectangle if failed or this property is unavailable. Supports `Au.lastError`.

#### Remarks

Calls `Au.elm.GetRect`. Most but not all UI elements support this property.