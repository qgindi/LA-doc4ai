# Enum `Au.Types.WSFlags`

Flags for `Au.wnd.SetStyle` and `Au.wnd.SetExStyle`.

```
[Flags]
public enum WSFlags
```

### Fields

| Name | Description |
| --- | --- |
| Add | Add the specified styles and don't change others. |
| NoException | Don't throw exception when fails. |
| Remove | Remove the specified styles and don't change others. |
| UpdateClient | Update client area. |
| UpdateNonclient | Update non-client area (frame, title bar). |