# Method `Au.More.RegisteredHotkey.Unregister`

Unregisters the hotkey.

```
public void Unregister()
```

#### Remarks

Called implicitly when disposing this variable. Must be called from the same thread as when registering, and the window must be still alive. If fails, calls `Au.print.warning`.