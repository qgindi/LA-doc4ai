# Method `Au.wnd.getwnd.top2`

Finds and returns the first non-topmost window in the Z order.

```
public static wnd top2(out wnd lastTopmost)
```

##### Parameters

- *lastTopmost*  (`Au.wnd`):
    Receives the last topmost window.

##### Returns

`Au.wnd`

#### Remarks

This function is slower than `Au.wnd.getwnd.top` etc. Enumerates windows, because there is no API to get directly.