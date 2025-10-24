# Method `Au.wnd.SetText`

Sets window/control name or control text.

```
public void SetText(string text)
```

##### Parameters

- *text*  (`string`):
    Text. Can be `null`, it is the same as `""`.

##### Exceptions

- `Au.Types.AuWndException`:
    Failed, for example the window is closed.

#### Remarks

Uses API `WM_SETTEXT`. Top-level window name usually its title bar text. For variable-text controls (edit, combo box, status bar, ...) this usually is the text that `Au.wnd.ControlText` would get. For other controls (button, static, ...) and top-level windows this usually is the text that `Au.wnd.Name` would get.

### See Also

`Au.wnd.GetText`

`Au.wnd.Name`

`Au.wnd.ControlText`