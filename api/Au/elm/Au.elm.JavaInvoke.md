# Method `Au.elm.JavaInvoke`

Performs one of actions supported by this Java UI element.

```
public void JavaInvoke(string action = null)
```

##### Parameters

- *action*  (`string`):
    Action name. See `Au.elm.DefaultAction`. If `null` (default), performs default action (like `Au.elm.Invoke`) or posts `Space` key message. More info in Remarks.

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Remarks

Read more about Java UI elements in `Au.elm` topic.

Problem: if the action opens a dialog, `Au.elm.Invoke`/`Au.elm.JavaInvoke(string)` do not return until the dialog is closed (or fail after some time). The caller then waits and cannot automate the dialog. Also then this process cannot exit until the dialog is closed. If the action parameter is `null` and the UI element is focusable, this function tries a workaround: it makes the UI element (button etc) focused and posts `Space` key message, which should press the button; then this function does not wait.