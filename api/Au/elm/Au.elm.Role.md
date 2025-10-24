# Property `Au.elm.Role`

Gets standard or custom role, as string.

```
public string Role { get; }
```

##### Property Value

`string`

`""` if failed. Supports `Au.lastError`.

#### Remarks

Most UI elements have a standard role, defined in enum `Au.Types.ERole` (except `None` and `Custom`). Some UI elements have a custom role, usually as string. For standard roles this function returns enum `Au.Types.ERole` member name. For string roles - the string. For unknown non-string roles - the `int` value like `"0"` or `"500"`. All UI elements must support this property. If failed, probably the `Au.elm` is invalid, for example the window is closed.