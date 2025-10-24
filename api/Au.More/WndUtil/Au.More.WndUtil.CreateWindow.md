# Method `Au.More.WndUtil.CreateWindow`

## Overload 1

Creates native/unmanaged window (API `CreateWindowEx`) and sets its window procedure.

```
public static wnd CreateWindow(WNDPROC wndProc, bool keepAlive, string className, string name = null, WS style = 0, WSE exStyle = 0, int x = 0, int y = 0, int width = 0, int height = 0, wnd parent = default, nint controlId = 0, nint hInstance = 0, nint param = 0)
```

##### Parameters

- *wndProc*  (`Au.Types.WNDPROC`):
    Window procedure.
- *keepAlive*  (`bool`):

    Protect *wndProc* from GC (garbage collector) until the window is destroyed (message `WM_NCDESTROY` received or thread ended).

    > **Important:**
    >     In some cases it may prevent destroying the window until thread ends, and it can be a big memory leak. For example WPF then does not destroy `HwndHost`-ed controls. Then let *keepAlive*=`false` and manually manage *wndProc* lifetime, for example keep it as a field of the wrapper class.
- *className*  (`string`)
- *name*  (`string`)
- *style*  (`Au.Types.WS`)
- *exStyle*  (`Au.Types.WSE`)
- *x*  (`int`)
- *y*  (`int`)
- *width*  (`int`)
- *height*  (`int`)
- *parent*  (`Au.wnd`)
- *controlId*  (`nint`)
- *hInstance*  (`nint`)
- *param*  (`nint`)

##### Returns

`Au.wnd`

##### Exceptions

- `Au.Types.AuException`:
    Failed to create window. Unlikely.

#### Remarks

If the class was registered with `Au.More.WndUtil.RegisterWindowClass` with `null` *wndProc*, the *wndProc* function will receive all messages. Else will not receive messages sent before `CreateWindowEx` returns (`WM_CREATE` etc).

To destroy the window can be used any function, including API `DestroyWindow`, `Au.More.WndUtil.DestroyWindow`, `Au.wnd.Close`, API `WM_CLOSE`.

* * *

## Overload 2

Creates native/unmanaged window.

```
public static wnd CreateWindow(string className, string name = null, WS style = 0, WSE exStyle = 0, int x = 0, int y = 0, int width = 0, int height = 0, wnd parent = default, nint controlId = 0, nint hInstance = 0, nint param = 0)
```

##### Parameters

- *className*  (`string`)
- *name*  (`string`)
- *style*  (`Au.Types.WS`)
- *exStyle*  (`Au.Types.WSE`)
- *x*  (`int`)
- *y*  (`int`)
- *width*  (`int`)
- *height*  (`int`)
- *parent*  (`Au.wnd`)
- *controlId*  (`nint`)
- *hInstance*  (`nint`)
- *param*  (`nint`)

##### Returns

`Au.wnd`

##### Exceptions

- `Au.Types.AuException`:
    Failed to create window. Unlikely.

#### Remarks

Calls API `CreateWindowEx`. To destroy the window can be used any function, including API `DestroyWindow`, `Au.More.WndUtil.DestroyWindow`, `Au.wnd.Close`, API `WM_CLOSE`.

### See Also

`Au.More.WndUtil.RegisterWindowClass`