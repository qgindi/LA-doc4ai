# Property `Au.wnd.focused`

Gets the control or window that has the keyboard input focus.

```
public static wnd focused { get; }
```

##### Property Value

`Au.wnd`

#### Remarks

The control/window can belong to any process/thread. With controls/windows of this thread you can use the more lightweight function `Au.wnd.thisThread.focused`. Calls API `GetGUIThreadInfo`.

### See Also

`Au.wnd.Focus`

`Au.wnd.IsFocused`