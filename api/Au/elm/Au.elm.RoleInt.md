# Property `Au.elm.RoleInt`

Gets role as enum `Au.Types.ERole`.

```
public ERole RoleInt { get; }
```

##### Property Value

`Au.Types.ERole`

0 (`ERole.None`) if failed. Supports `Au.lastError`.

#### Remarks

Most UI elements have a standard role, defined in enum `Au.Types.ERole` (except `None` and `Custom`). Some UI elements have a custom role, usually as string; then returns `ERole.Custom`. All UI elements must support this property. If failed, probably the `Au.elm` is invalid, for example the window is closed.