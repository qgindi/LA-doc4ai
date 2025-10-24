# Method `Au.wnd.SetWindowPos`

Calls API `SetWindowPos`.

```
public bool SetWindowPos(SWPFlags swpFlags, int x = 0, int y = 0, int cx = 0, int cy = 0, wnd zorderAfter = default)
```

##### Parameters

- *swpFlags*  (`Au.Types.SWPFlags`)
- *x*  (`int`)
- *y*  (`int`)
- *cx*  (`int`)
- *cy*  (`int`)
- *zorderAfter*  (`Au.wnd`):
    A window or a constant from `Au.Types.SpecHWND` (`TOP`, `BOTTOM`, `TOPMOST`, `NOTOPMOST`).

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.