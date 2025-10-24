# Method `Au.wnd.Focus`

Sets the keyboard input focus to this control. Also activates its top-level parent window (see `Au.wnd.Activate`).

```
public void Focus()
```

##### Exceptions

- `Au.Types.AuWndException`:

    - Invalid handle.
    - Disabled.
    - Failed to set focus.
    - Failed to activate parent window.
- `Au.Types.InputDesktopException`

#### Remarks

The control can belong to any process/thread. With controls of this thread you can use the more lightweight function `Au.wnd.thisThread.focus`. Works not with all windows. For example, does not work with Windows Store apps. Then use `Au.elm.Focus`. Can instead focus a child control. For example, if this is a combo box, it will focus its child Edit control. Then does not throw exception. This can be control or top-level window. Top-level windows also can have focus. Fails when the target process is admin or uiAccess and this process isn't. See [UAC](../articles/UAC.html).

### See Also

`Au.wnd.focused`

`Au.wnd.IsFocused`

`Au.elm.Focus`