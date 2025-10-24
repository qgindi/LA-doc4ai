# Property `Au.wnd.IsCloaked`

Detects whether the window is cloaked (it's a way to hide a window).

```
public bool IsCloaked { get; }
```

##### Property Value

`bool`

`true` if the window is cloaked. `false` if not cloaked or if failed.

#### Remarks

On Windows 7 returns `false` because there is no "cloaked window" feature. Windows 10 uses window cloaking mostly to hide windows on inactive desktops. Windows 8 - mostly to hide Windows Store app windows.

### See Also

`Au.wnd.IsCloakedGetState`