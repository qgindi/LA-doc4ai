# Property `Au.More.WindowsHook.LowLevelHooksTimeout`

Gets the max time in milliseconds allowed by Windows for low-level keyboard and mouse hook procedures.

```
public static int LowLevelHooksTimeout { get; }
```

##### Property Value

`int`

#### Remarks

Gets registry value `HKEY_CURRENT_USER\Control Panel\Desktop:LowLevelHooksTimeout`. If it is missing, returns 300; it is the default value used by Windows. If greater than 1000, returns 1000, because Windows 10 ignores bigger values.

If a hook procedure takes more time, Windows does not wait. Then its return value is ignored, and the event is passed to other apps, hooks, etc. After several such cases Windows may fully or partially disable the hook. This class detects such cases; then restores the hook and prints a warning. If the warning is rare, you can ignore it. If frequent, it means your hook procedure is too slow.

Callback functions of keyboard and mouse triggers are called in a hook procedure, therefore must be as fast as possible. More info: `Au.Triggers.TriggerFuncs`.

More info: [registry LowLevelHooksTimeout](https://www.google.com/search?q=registry+LowLevelHooksTimeout+site:microsoft.com).

Note: After changing the timeout in registry, it is not applied immediately. Need to log off/on.