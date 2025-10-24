# Method `Au.wnd.ResizeClient`

Resizes this window to match the specified client area size. Calls `Au.wnd.ResizeL`.

```
public void ResizeClient(int? width, int? height)
```

##### Parameters

- *width*  (`int?`):
    Client area width. Use `null` to not change.
- *height*  (`int?`):
    Client area height. Use `null` to not change.

##### Exceptions

- `Au.Types.AuWndException`