# Property `Au.wnd.getwnd.top`

Gets the first top-level window in the Z order.

```
public static wnd top { get; }
```

##### Property Value

`Au.wnd`

#### Remarks

Probably it is a topmost window. To get the first non-topmost window, use `Au.wnd.getwnd.top2`. Calls API `GetTopWindow`.