# Method `Au.wnd.Activate`

Activates this window. Also makes it visible and not minimized. The active window is in the foreground and receives keyboard and mouse input.

```
public wnd Activate()
```

##### Returns

`Au.wnd`

Self.

##### Exceptions

- `Au.Types.AuWndException`:
    Failed to activate.
- `Au.Types.InputDesktopException`

#### Remarks

Activating a window usually also uncloaks it, for example switches to its virtual desktop on Windows 10/11. Fails (throws exception) if cannot activate this window, except:

- When this is a control. Then activates its top-level parent window.
- When the window's process instead activates another window of the same thread.
- If this is `Au.wnd.getwnd.root`, just deactivates the currently active window.

### See Also

`Au.wnd.ActivateL`

`Au.wnd.IsActive`

`Au.wnd.active`

`Au.wnd.switchActiveWindow`