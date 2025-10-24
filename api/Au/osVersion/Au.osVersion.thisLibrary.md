# Property `Au.osVersion.thisLibrary`

Gets the version string of this library (`Au.dll`), like `"1.2.3"`.

```
public static string thisLibrary { get; }
```

##### Property Value

`string`

#### Remarks

This function is fast, unlike `typeof(osVersion).Assembly.GetName().Version.ToString(3)`.

LibreAutomate uses `Au.dll` of the same version as of LibreAutomate.