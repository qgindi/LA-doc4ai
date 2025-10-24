# Method `Au.More.WndSavedRect.NormalizeRect`

Gets real rectangle for restoring saved window rectangle.

```
public RECT NormalizeRect()
```

##### Returns

`Au.Types.RECT`

#### Remarks

It is recommended to call this before creating window, and create window with the returned rectangle. Also set maximized state if `Au.More.WndSavedRect.Maximize`. If it is not possible, can be called later, for example when window is created but still invisible. However then possible various problems, for example may need to set window rectangle two times, because the window may be for example DPI-scaled when moving to another screen etc.

This function ensures the window is in screen, ensures correct size when screen DPI changed, etc.