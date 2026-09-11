# Method `Au.wnd.SetStyle`

Changes window style.

```csharp
public WS SetStyle(WS style, WSFlags flags = 0)
```

##### Parameters

- *style*  (`Au.Types.WS`):
  One or more `Au.Types.WS` flags and/or class-specific style flags. Reference: [window styles](🔗).
- *flags*  (`Au.Types.WSFlags`):
  Enum: Add, Remove, UpdateNonclient, UpdateClient, NoException.

##### Returns

`Au.Types.WS`

Previous value.

##### Exceptions

- `Au.Types.AuWndException`

### See Also

`Au.wnd.Style`