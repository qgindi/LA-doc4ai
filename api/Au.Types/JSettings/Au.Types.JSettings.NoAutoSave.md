# Property `Au.Types.JSettings.NoAutoSave`

Don't automatically call `Au.Types.JSettings.SaveIfNeed`. If `false` (default), calls every 2 s (unless `Au.Types.JSettings.NoAutoSaveTimer` `true`); also when disposing and when the process exits.

```
protected bool NoAutoSave { get; set; }
```

##### Property Value

`bool`