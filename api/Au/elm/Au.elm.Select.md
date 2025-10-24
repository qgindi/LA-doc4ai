# Method `Au.elm.Select`

Selects or deselects.

```
public void Select(ESelect how = ESelect.TAKESELECTION)
```

##### Parameters

- *how*  (`Au.Types.ESelect`):
    Specifies whether to select, focus, add to selection etc. Can be two flags, for example `ESelect.TAKEFOCUS | ESelect.TAKESELECTION`. With flag `TAKEFOCUS` activates the window like `Au.elm.Focus`.

##### Exceptions

- `Au.Types.AuException`:
    Failed.
- `Au.Types.AuWndException`:
    Failed to activate the window (`Au.wnd.Activate`) or focus the control (`Au.wnd.Focus`).

#### Remarks

Not all UI elements support it. Most UI elements support not all flags. It depends on `Au.Types.EState` `FOCUSABLE`, `SELECTABLE`, `MULTISELECTABLE`, `EXTSELECTABLE`, `DISABLED`. Many UI elements have bugs, especially with flag `TAKEFOCUS`. More bugs when the UI element has been found with flag `Au.Types.EFFlags.NotInProc`.