# Method `Au.wnd.thisThread.focus`

Calls API `SetFocus`. It sets the keyboard input focus to the specified control or window, which must be of this thread.

```
public static bool focus(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

#### Remarks

Fails if the control/window belongs to another thread or is invalid or disabled. Can instead focus a child control. For example, if combo box, will focus its child Edit control. Then returns `true`.