# Method `Au.wnd.SetExStyle`

Changes window extended style.

```csharp
public WSE SetExStyle(WSE style, WSFlags flags = 0)
```

##### Parameters

- *style*  (`Au.Types.WSE`):
  One or more `Au.Types.WSE` flags. Reference: [extended window styles](🔗).
- *flags*  (`Au.Types.WSFlags`):
  Enum: Add, Remove, UpdateNonclient, UpdateClient, NoException.

##### Returns

`Au.Types.WSE`

Previous value.

##### Exceptions

- `Au.Types.AuWndException`

### See Also

`Au.wnd.ExStyle`