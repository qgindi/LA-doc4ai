# Method `Au.Types.ExtWpf.Hwnd`

Gets native window handle of this `System.Windows.Window` or `System.Windows.Controls.Primitives.Popup`, or container window handle of this child object.

```
public static wnd Hwnd(this DependencyObject t)
```

##### Parameters

- *t*  (`DependencyObject`)

##### Returns

`Au.wnd`

`default(wnd)` if:

- called before creating or after closing real window;
- failed;
- *t* is `null`.