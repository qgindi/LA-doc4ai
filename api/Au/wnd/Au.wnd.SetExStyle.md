# Method `Au.wnd.SetExStyle`

Changes window extended style.

```
public WSE SetExStyle(WSE style, WSFlags flags = 0)
```

##### Parameters

- *style*  (`Au.Types.WSE`):
    One or more `Au.Types.WSE` flags. Reference: [extended window styles](https://www.google.com/search?q=extended+window+styles+site:microsoft.com).
- *flags*  (`Au.Types.WSFlags`)

##### Returns

`Au.Types.WSE`

Previous value.

##### Exceptions

- `Au.Types.AuWndException`

### See Also

`Au.wnd.ExStyle`