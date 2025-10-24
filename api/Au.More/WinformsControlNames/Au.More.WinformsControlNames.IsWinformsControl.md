# Method `Au.More.WinformsControlNames.IsWinformsControl`

Returns `true` if window class name starts with `"WindowsForms"`. Usually it means that we can get Windows Forms control name of *w* and its child controls.

```
public static bool IsWinformsControl(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`):
    The window. Can be top-level or control.

##### Returns

`bool`