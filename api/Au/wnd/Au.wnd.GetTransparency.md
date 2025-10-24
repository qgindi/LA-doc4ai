# Method `Au.wnd.GetTransparency`

Gets window transparency attributes (opacity and transparency color).

```
public bool GetTransparency(out int? opacity, out ColorInt? colorKey)
```

##### Parameters

- *opacity*  (`int?`):
    If this function returns `true` and the window has an opacity attribute, receives the opacity value 0-255, else `null`.
- *colorKey*  (`Au.Types.ColorInt?`):
    If this function returns `true` and the window has a transparency color attribute, receives the color, else `null`.

##### Returns

`bool`

True if the window has transparency attributes set with `Au.wnd.SetTransparency` or API `SetLayeredWindowAttributes`. Supports `Au.lastError`.

#### Remarks

Uses API `GetLayeredWindowAttributes`.