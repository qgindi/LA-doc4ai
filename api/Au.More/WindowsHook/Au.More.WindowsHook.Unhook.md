# Method `Au.More.WindowsHook.Unhook`

Removes the hook.

```
public void Unhook()
```

#### Remarks

Does nothing if already removed or wasn't set. Later you can call `Au.More.WindowsHook.Hook` to set hook again. Note: call `Au.More.WindowsHook.Dispose` instead if will not need to hook again.