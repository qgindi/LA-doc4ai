# Property `Au.wnd.IsAlive`

Returns `true` if the window exists (the window handle is valid). Returns `false` if the handle is 0 or invalid. Invalid non-0 handle usually means that the window is closed/destroyed.

```
public bool IsAlive { get; }
```

##### Property Value

`bool`

#### Remarks

Calls `Au.wnd.Is0` and API `IsWindow`. Although a `Au.wnd` variable holds a window handle, which is like a reference to a window, it does not prevent closing that window and making the handle invalid. After closing the window, the OS can even assign the same handle value to a new window, although normally it can happen only after long time.

> **Note:**
> Use this carefully with windows of other applications or threads. The window can be closed at any moment, even when your thread is still in this function.