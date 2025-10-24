# Property `Au.wnd.active`

Gets the active (foreground) window. Calls API `GetForegroundWindow`.

```
public static wnd active { get; }
```

##### Property Value

`Au.wnd`

Returns `default(wnd)` if there is no active window; more info: `Au.More.WndUtil.WaitForAnActiveWindow`.