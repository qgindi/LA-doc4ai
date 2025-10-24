# Property `Au.wnd.Name`

Gets name.

```
public string Name { get; }
```

##### Property Value

`string`

Returns `""` if no name. Returns `null` if failed, eg if the window is closed. Supports `Au.lastError`.

#### Remarks

Top-level window name usually its title bar text. Control name usually is its text that does not change, for example button or static (label) control text. Unlike `Au.wnd.ControlText`, this function usually does not get variable text, for example Edit control editable text, combo box control selected item text, status bar text. Calls `Au.wnd.GetText(false, true)`.

### See Also

`Au.wnd.SetText`

`Au.wnd.ControlText`

`Au.wnd.NameElm`

`Au.wnd.NameWinforms`