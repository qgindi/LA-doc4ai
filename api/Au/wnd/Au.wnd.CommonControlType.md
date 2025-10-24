# Property `Au.wnd.CommonControlType`

If this control is (or is based on) a standard control provided by Windows, such as button or treeview, returns the control type. Else returns `None`.

```
public WControlType CommonControlType { get; }
```

##### Property Value

`Au.Types.WControlType`

#### Remarks

Sends message `WM_GETOBJECT` `QUERYCLASSNAMEIDX`. Slower than `Au.wnd.ClassName` or `Au.wnd.ClassNameIs`, but can detect the base type of controls based on standard Windows controls but with a different class name.