# Method `Au.More.WndUtil.RegisterWindowClass`

Registers new window class in this process.

```
public static void RegisterWindowClass(string className, WNDPROC wndProc = null, RWCEtc etc = null)
```

##### Parameters

- *className*  (`string`):
    Class name.
- *wndProc*  (`Au.Types.WNDPROC`):

    Delegate of a window procedure. See [Window Procedures](https://www.google.com/search?q=Window+Procedures+site:microsoft.com).

    Use `null` when you need a different delegate (method or target object) for each window instance; create windows with `Au.More.WndUtil.CreateWindow` or `Au.More.WndUtil.CreateMessageOnlyWindow`. If not `null`, it must be a static named method; create windows with any other function, including API `CreateWindowEx`.
- *etc*  (`Au.Types.RWCEtc`):
    Can be used to specify API `WNDCLASSEX` fields. To set cursor use field `mCursor` (standard cursor) or `hCursor` (native handle of a custom cursor). If `null`, this function sets arrow cursor and style `CS_VREDRAW | CS_HREDRAW`.

##### Exceptions

- `ArgumentException`:
    *wndProc* is an instance method. Must be static method or `null`. If need instance method, use `null` here and pass *wndProc* to `Au.More.WndUtil.CreateWindow`.
- `InvalidOperationException`:
    The class already registered with this function and different *wndProc* (another method or another target object).
- `Win32Exception`:
    Failed, for example if the class already exists and was registered not with this function.

#### Remarks

Calls API `RegisterClassEx`. The window class is registered until this process ends. Don't need to unregister. If called next time for the same window class, does nothing if *wndProc* is equal to the previous (or both `null`). Then ignores *etc*. Throws exception if different. Thread-safe. Protects the *wndProc* delegate from GC.