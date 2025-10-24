# Property `Au.toolbar.MaximizedWindowTopPlus`

Number of pixels to add to the top of the retrieved rectangle of the owner window when it is maximized. That is, move this toolbar slightly down (if positive) or up (if negative).

```
public double MaximizedWindowTopPlus { get; set; }
```

##### Property Value

`double`

#### Remarks

When you create a toolbar attached to a window, and the anchor is at the top, test whether it is in visually the same vertical position (relative to UI elements of the window) when the window is maximized and when not maximized. On some windows it will be in a different position, and it is not what you want. Reason: some windows, when maximized, draw their UI elements in a different vertical position than when not maximized. It's impossible to reliably correct it automatically. To correct it, set this property before calling `Au.toolbar.Show` or `Au.toolbar.Show`. With most such windows, the good value is 6.7 or 7.5. With some windows may need a negative value.

By default the value is logical pixels; that is, will be scaled depending on DPI.

If the owner window has multiple attached toolbars and all they run in the same thread, set this property for one of them, not for all. It will adjust the vertical position of all them.

With some windows can be used another way to correct the vertical position: call `Au.toolbar.Show` with `clientArea: true`.

If neither way works, use `Au.toolbar.Show` (you'll need to create a class that implements `Au.Types.ITBOwnerObject`). For example, to move the toolbar to a different position when the window is in full-screen mode.