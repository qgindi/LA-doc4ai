# Property `Au.screen.all`

Gets all screens.

```
public static screen[] all { get; }
```

##### Property Value

`Au.screen[]`

#### Remarks

The order of array elements may be different than in Windows Settings. The primary screen is always at index 0. The array is not cached. Each time calls API `EnumDisplayMonitors`.