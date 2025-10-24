# Method `Au.More.Dpi.AdjustWindowRectEx`

Calls API `AdjustWindowRectExForDpi` if available, else `AdjustWindowRectEx`.

```
public static bool AdjustWindowRectEx(DpiOf dpiOf, ref RECT r, WS style, WSE exStyle, bool hasMenu = false)
```

##### Parameters

- *dpiOf*  (`Au.Types.DpiOf`)
- *r*  (`Au.Types.RECT`)
- *style*  (`Au.Types.WS`)
- *exStyle*  (`Au.Types.WSE`)
- *hasMenu*  (`bool`)

##### Returns

`bool`

#### Remarks

Also adds scrollbar width or/and height if need.