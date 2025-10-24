# Method `Au.Types.ExtMisc.Hwnd`

Gets window handle as `Au.wnd`.

```
public static wnd Hwnd(this Control t, bool create = false)
```

##### Parameters

- *t*  (`Control`):
    A `Control` or `Form` etc. Cannot be `null`.
- *create*  (`bool`):
    Create handle if still not created. Default `false` (return `default(wnd)`). Unlike `System.Windows.Forms.Control.CreateControl`, creates handle even if invisible. Does not create child control handles.

##### Returns

`Au.wnd`

#### Remarks

Should be called in control's thread. Calls `System.Windows.Forms.Control.IsHandleCreated` and `System.Windows.Forms.Control.Handle`.