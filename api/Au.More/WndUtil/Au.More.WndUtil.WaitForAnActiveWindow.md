# Method `Au.More.WndUtil.WaitForAnActiveWindow`

Waits while there is no active window.

```
public static bool WaitForAnActiveWindow(bool doEvents = false)
```

##### Parameters

- *doEvents*  (`bool`):
    While waiting call `Au.wait.doEvents` to process Windows messages etc.

##### Returns

`bool`

#### Remarks

When there is no active window, functions `Au.wnd.active` and API `GetForegroundWindow` return 0. It sometimes happens after closing, minimizing or switching the active window, briefly until another window becomes active. This function waits max 500 ms, then returns `false` if there is no active window. Don't need to call this after calling functions of this library.