# Method `Au.mouse.isPressed`

Returns `true` if some mouse buttons are pressed.

```
public static bool isPressed(MButtons buttons = MButtons.Left | MButtons.Right | MButtons.Middle | MButtons.X1 | MButtons.X2)
```

##### Parameters

- *buttons*  (`Au.Types.MButtons`):
    Return `true` if some of these buttons are down. Default: any.

##### Returns

`bool`

#### Remarks

Uses API `GetAsyncKeyState`. When processing user input in UI code (forms, WPF), instead use class `Au.keys.gui` or .NET functions. They use API `GetKeyState`. When mouse left and right buttons are swapped, gets logical state, not physical.

### See Also

`Au.mouse.waitForNoButtonsPressed`