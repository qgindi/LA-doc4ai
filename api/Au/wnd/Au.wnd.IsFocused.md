# Property `Au.wnd.IsFocused`

Returns `true` if this is the control or window that has the keyboard input focus.

```
public bool IsFocused { get; }
```

##### Property Value

`bool`

#### Remarks

This control/window can belong to any process/thread. With controls/windows of this thread you can use the more lightweight function `Au.wnd.thisThread.isFocused`. Calls `Au.wnd.focused`.

### See Also

`Au.wnd.Focus`