# Property `Au.wnd.IsUwpApp`

On Windows 10 and later returns non-zero if this top-level window is a UWP app window: 1 if class name is `"ApplicationFrameWindow"`, 2 if `"Windows.UI.Core.CoreWindow"`.

```
public int IsUwpApp { get; }
```

##### Property Value

`int`

### See Also

`Au.More.WndUtil.GetWindowsStoreAppId`