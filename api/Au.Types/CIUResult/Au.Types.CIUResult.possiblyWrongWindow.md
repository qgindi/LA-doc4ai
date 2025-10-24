# Field `Au.Types.CIUResult.possiblyWrongWindow`

If `true`, most likely `Au.Types.CIUResult.w` is incorrect window, because the window that was there before capturing disappeared while capturing, for example it was a popup menu. If captured from screen (without flags like `WindowDC`), `Au.Types.CIUResult.w` may be correct even if this is `true` (can't detect reliably), else certainly incorrect.

```
public bool possiblyWrongWindow
```