# Method `Au.wnd.Resize`

Resizes.

```
public void Resize(Coord width, Coord height, bool workArea = false, screen screen = default, bool visibleRect = false)
```

##### Parameters

- *width*  (`Au.Types.Coord`):
    Width. If `default`, does not change width.
- *height*  (`Au.Types.Coord`):
    Height. If `default`, does not change height.
- *workArea*  (`bool`):
    For `Au.Types.Coord.Fraction` etc use width/height of the work area. This parameter not used with child windows.
- *screen*  (`Au.screen`):
    For `Au.Types.Coord.Fraction` etc use width/height of this screen. Default - primary. Example: `screen.index(1)`. This parameter not used with child windows.
- *visibleRect*  (`bool`):
    Use the visible rectangle without the transparent frame. Note: the window should be visible. This parameter not used with child windows.

##### Exceptions

- `Au.Types.AuWndException`

#### Remarks

Also restores the visible top-level window if it is minimized or maximized. With windows of current thread usually it's better to use `Au.wnd.ResizeL`.