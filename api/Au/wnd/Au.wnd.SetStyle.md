# Method `Au.wnd.SetStyle`

Changes window style.

```
public WS SetStyle(WS style, WSFlags flags = 0)
```

##### Parameters

- *style*  (`Au.Types.WS`):
    One or more `Au.Types.WS` flags and/or class-specific style flags. Reference: [window styles](https://www.google.com/search?q=window+styles+site:microsoft.com).
- *flags*  (`Au.Types.WSFlags`)

##### Returns

`Au.Types.WS`

Previous value.

##### Exceptions

- `Au.Types.AuWndException`

### See Also

`Au.wnd.Style`