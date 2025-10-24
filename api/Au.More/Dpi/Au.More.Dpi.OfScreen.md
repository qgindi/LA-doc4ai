# Method `Au.More.Dpi.OfScreen`

Gets DPI of a screen.

```
public static int OfScreen(nint hMonitor, bool supportWin81 = false)
```

##### Parameters

- *hMonitor*  (`nint`):
    Native screen handle (`HMONITOR`).
- *supportWin81*  (`bool`):
    Support Windows 8.1 and later. If `false` (default), supports Windows 10 1607 and later.

##### Returns

`int`

`Au.More.Dpi.System` if fails or if not supported on this Windows version.

#### Remarks

Uses API `GetDpiForMonitor`.

### See Also

`Au.screen.Dpi`