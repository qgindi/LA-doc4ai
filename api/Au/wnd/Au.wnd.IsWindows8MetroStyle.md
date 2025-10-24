# Property `Au.wnd.IsWindows8MetroStyle`

Returns `true` if this window has Metro style, ie is not a classic desktop window.

```
public bool IsWindows8MetroStyle { get; }
```

##### Property Value

`bool`

#### Remarks

On Windows 8/8.1 most Windows Store app windows and many shell windows have Metro style. On Windows 10 few windows have Metro style. On Windows 7 there are no Metro style windows.

### See Also

`Au.More.WndUtil.GetWindowsStoreAppId`