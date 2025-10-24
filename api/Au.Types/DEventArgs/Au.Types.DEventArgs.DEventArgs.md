# Constructor of `Au.Types.DEventArgs`

```
public DEventArgs(dialog d, wnd hwnd, DNative.TDN message, nint wParam, int Button, int TimerTimeMS, string LinkHref)
```

##### Parameters

- *d*  (`Au.dialog`):
    The dialog.
- *hwnd*  (`Au.wnd`):
    The dialog window.
- *message*  (`Au.Types.DNative`.`Au.Types.DNative.TDN`):
    See [task dialog notifications](https://www.google.com/search?q=task+dialog+notifications+site:microsoft.com).
- *wParam*  (`nint`):
    See [task dialog notifications](https://www.google.com/search?q=task+dialog+notifications+site:microsoft.com).
- *Button*  (`int`):
    In a `Au.dialog.ButtonClicked` event handler - button id.
- *TimerTimeMS*  (`int`):
    In a `Au.dialog.Timer` event handler - timer time in milliseconds. The handler can set `returnValue` = 1 to reset this.
- *LinkHref*  (`string`):
    In an `Au.dialog.HyperlinkClicked` event handler - the `href` attribute.