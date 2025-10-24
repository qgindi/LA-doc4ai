# Property `Au.folders.noAutoCreate`

Don't auto-create folders when accessing `Au.folders.ThisAppDocuments`, `Au.folders.ThisAppTemp`, `Au.folders.ThisAppDataLocal` or `Au.folders.ThisAppDataRoaming` in this thread.

```
public static bool noAutoCreate { get; set; }
```

##### Property Value

`bool`

#### Remarks

Normally this is used temporarily, then restored (set = `false`).