# Method `Au.More.WndUtil.Subclass`

Subclasses a window.

```
public static object Subclass(wnd w, WNDPROC proc)
```

##### Parameters

- *w*  (`Au.wnd`):
    A window or control of this thread.
- *proc*  (`Au.Types.WNDPROC`):
    The new window procedure. It is called on every message received by the window (unless blocked by another subclass added later). Let it call `Au.More.WndUtil.DefSubclassProc`, except when you want to block the message.

##### Returns

`object`

A cookie for `Au.More.WndUtil.Unsubclass`. Returns `null` if failed.

#### Remarks

Uses API `SetWindowSubclass`. Implicitly unsubclasses when the window is destroyed. Protects *proc* from GC for as long as need.