# Method `Au.dialog.InScreen`

Sets the screen (display monitor) where to show the dialog in multi-screen environment.

```
public dialog InScreen(screen screen)
```

##### Parameters

- *screen*  (`Au.screen`)

##### Returns

`Au.dialog`

#### Remarks

If not set, will be used owner window's screen or `Au.dialog.options.defaultScreen`. More info: `Au.screen`, `Au.wnd.MoveInScreen`.