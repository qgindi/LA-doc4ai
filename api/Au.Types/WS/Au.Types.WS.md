# Enum `Au.Types.WS`

Window styles.

```
[Flags]
public enum WS : uint
```

##### Remarks

Reference: [Window Styles](https://www.google.com/search?q=Window+Styles+site:microsoft.com). Here names are without prefix `WS_`. For example, instead of `WS_BORDER` use `WS.BORDER`. Not included constants that are 0 (eg `WS_TILED`) or are duplicate (eg `WS_SIZEBOX` is same as `WS_THICKFRAME`) or consist of multiple other constants (eg `WS_TILEDWINDOW`).

### Fields

| Name | Description |
| --- | --- |
| BORDER |  |
| CAPTION |  |
| CHILD |  |
| CLIPCHILDREN |  |
| CLIPSIBLINGS |  |
| DISABLED |  |
| DLGFRAME |  |
| GROUP |  |
| HSCROLL |  |
| MAXIMIZE |  |
| MAXIMIZEBOX |  |
| MINIMIZE |  |
| MINIMIZEBOX |  |
| POPUP |  |
| SYSMENU |  |
| TABSTOP |  |
| THICKFRAME |  |
| VISIBLE |  |
| VSCROLL |  |