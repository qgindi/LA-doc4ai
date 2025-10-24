# Property `Au.elm.UiaCN`

Gets the UI Automation `ClassName` property.

```
public string UiaCN { get; }
```

##### Property Value

`string`

`""` if this property is unavailable or if failed. Supports `Au.lastError`.

#### Remarks

Only UI elements found with flag `Au.Types.EFFlags.UIA` can have this property.