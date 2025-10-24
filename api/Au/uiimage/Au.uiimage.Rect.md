# Property `Au.uiimage.Rect`

Gets location of the found image, relative to the search area.

```
public RECT Rect { get; init; }
```

##### Property Value

`Au.Types.RECT`

#### Remarks

Relative to the window/control client area (if area type is `Au.wnd`), UI element (if `Au.elm`), image (if `System.Drawing.Bitmap`) or screen (if `Au.Types.RECT`). More info: `Au.uiimage.find`.