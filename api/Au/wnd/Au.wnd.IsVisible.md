# Property `Au.wnd.IsVisible`

Returns `true` if the window is visible. Returns `false` if is invisible or is a child of invisible parent. Also returns `false` when fails (probably window closed or 0 handle). Supports `Au.lastError`.

```
public bool IsVisible { get; }
```

##### Property Value

`bool`

#### Remarks

Calls API `IsWindowVisible`. Does not call `Au.wnd.IsCloaked`.

Even when this function returns `true`, the window may be actually invisible. It can be cloaked, on an inactive Windows 10 virtual desktop (cloaked), inactive Windows Store app (cloaked), transparent, zero-size, minimized, off-screen, covered by other windows or can have zero-size window region.

### See Also

`Au.wnd.IsCloaked`

`Au.wnd.IsVisibleAndNotCloaked`

`Au.wnd.Show`

`Au.wnd.Activate`