# Property `Au.elm.Value`

Gets or sets value.

```
public string Value { get; set; }
```

##### Exceptions

- `Au.Types.AuException`:
    Failed to set value.

##### Property Value

`string`

#### Remarks

Usually it is editable text or some other value that can be changed at run time, therefore in most cases it cannot be used to find or identify the UI element reliably. The `get` function returns `""` if this property is unavailable or if failed. Supports `Au.lastError`. Most UI elements don't support `set`.