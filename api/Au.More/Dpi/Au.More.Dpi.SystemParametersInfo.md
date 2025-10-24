# Method `Au.More.Dpi.SystemParametersInfo`

Calls API `SystemParametersInfoForDpi` if available, else `SystemParametersInfo`. Use only with *uiAction* = `SPI_GETICONTITLELOGFONT`, `SPI_GETICONMETRICS`, `SPI_GETNONCLIENTMETRICS`.

```
public static bool SystemParametersInfo(uint uiAction, int uiParam, void* pvParam, DpiOf dpiOf)
```

##### Parameters

- *uiAction*  (`uint`)
- *uiParam*  (`int`)
- *pvParam*  (`void*`)
- *dpiOf*  (`Au.Types.DpiOf`)

##### Returns

`bool`