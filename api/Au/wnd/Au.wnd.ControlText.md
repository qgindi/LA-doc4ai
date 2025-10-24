# Property `Au.wnd.ControlText`

Gets control text.

```
public string ControlText { get; }
```

##### Property Value

`string`

Returns `""` if no text. Returns `null` if failed, eg if the window is closed. Supports `Au.lastError`.

#### Remarks

Unlike `Au.wnd.Name`, this function prefers variable text, for example Edit control text, combo box selected item text, status bar text. For controls that cannot have such text (eg button, static), it usually gets the same text as `Name`. For example button and static (label) controls. Much slower than `Name`. Fails if the window is hung. Calls `Au.wnd.GetText(true, false)`.

### See Also

`Au.wnd.SetText`

`Au.wnd.Name`