# Property `Au.Types.JSettings.LoadedFile`

`true` if settings were loaded from file.

```
[JsonIgnore]
public bool LoadedFile { get; }
```

##### Property Value

`bool`

#### Remarks

Returns `false` if `Au.Types.JSettings.Load<T>` did not find the file (the settings were not saved) or failed to load/parse or parameter *useDefault* = `true` or parameter *file* = `null`.