# Method `Au.elm.fromWindow`

Gets UI element of window or control. Or some its standard part - client area, titlebar etc.

```
public static elm fromWindow(wnd w, EObjid objid = EObjid.WINDOW, EWFlags flags = 0)
```

##### Parameters

- *w*  (`Au.wnd`):
    Window or control.
- *objid*  (`Au.Types.EObjid`):
    Window part id. Default `EObjid.WINDOW`. Also can be a custom id supported by that window, cast `int` to `EObjid`.
- *flags*  (`Au.Types.EWFlags`):
    Flags.

##### Returns

`Au.elm`

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid window.
- `Au.Types.AuException`:
    Failed. For example, window of a higher [UAC](../articles/UAC.html) integrity level process.
- `ArgumentException`:
    *objid* is `QUERYCLASSNAMEIDX` or `NATIVEOM`.

#### Remarks

Uses API `AccessibleObjectFromWindow`.