# Method `Au.wnd.SetTransparency`

Sets window transparency attributes (opacity and/or transparent color).

```
public void SetTransparency(bool allowTransparency, int? opacity = null, ColorInt? colorKey = null, bool noException = false)
```

##### Parameters

- *allowTransparency*  (`bool`):
    Set or remove `WS_EX_LAYERED` style that is required for transparency. If `false`, other parameters are not used.
- *opacity*  (`int?`):
    Opacity from 0 (completely transparent) to 255 (opaque). Does not change if `null`. If less than 0 or greater than 255, makes 0 or 255.
- *colorKey*  (`Au.Types.ColorInt?`):
    Make pixels of this color completely transparent. Does not change if `null`. The alpha byte is not used.
- *noException*  (`bool`):
    Don't throw exception when fails.

##### Exceptions

- `Au.Types.AuWndException`

#### Remarks

Uses API `SetLayeredWindowAttributes`. On Windows 7 works only with top-level windows, not with controls. Fails with WPF windows (class name starts with `"HwndWrapper"`).