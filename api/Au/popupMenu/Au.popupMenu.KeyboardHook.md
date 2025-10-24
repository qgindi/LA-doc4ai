# Property `Au.popupMenu.KeyboardHook`

Gets or sets callback function that decides how to respond to pressed keys (default, close, ignore, block).

```
public Func<popupMenu, HookData.Keyboard, PMKHook> KeyboardHook { get; set; }
```

##### Property Value

`Func<Au.popupMenu, Au.Types.HookData.Au.Types.HookData.Keyboard, Au.Types.PMKHook>`

#### Remarks

The function is called on each key down event while the menu is open. Only if current thread is not in the foreground. To block a key, call `Au.Types.HookData.Keyboard.BlockEvent`. The function must be as fast as possible.