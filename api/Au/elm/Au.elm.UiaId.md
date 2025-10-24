# Property `Au.elm.UiaId`

Gets the UI Automation `AutomationId` property.

```
public string UiaId { get; }
```

##### Property Value

`string`

`""` if this property is unavailable or if failed. Supports `Au.lastError`.

#### Remarks

Only UI elements found with flag `Au.Types.EFFlags.UIA` can have this property.