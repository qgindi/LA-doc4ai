# Property `Au.wnd.IsCloakedGetState`

Gets the cloaked state (it's a way to hide a window).

```
public int IsCloakedGetState { get; }
```

##### Property Value

`int`

- 0 if not cloaked or if failed.
- 1 cloaked by its application.
- 2 cloaked by Windows.
- 4 cloaked because its owner window is cloaked.

On Windows 7 returns 0 because there is no "cloaked window" feature.

### See Also

`Au.wnd.IsCloaked`