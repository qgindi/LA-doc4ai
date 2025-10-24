# Class `Au.keys`

Keyboard functions. Send virtual keystrokes and text to the active window, get key state, wait for key.

```
public class keys
```

##### Remarks

The main function is `Au.keys.send`. Most documentation is there. See also `Au.keys.sendt`. These functions use `Au.opt.key`. Alternatively can be used `keys` variables, see `Au.keys.keys`.

##### Examples

```
keys.send("Ctrl+Shift+Left"); //press Ctrl+Shift+Left

opt.key.KeySpeed = 300; //set options for static functions
keys.send("Ctrl+A Del Tab*3", "!text", "Enter", 500); //press Ctrl+A, Del, Tab 3 times, send text, Enter, wait 500 ms

keys.sendt("text\r\n"); //send text that ends with newline
```

##### Inheritance

`object` → `keys`

### Constructors

`keys(OKey)`

### Properties

`Options`, `isAlt`, `isCapsLock`, `isCtrl`, `isNumLock`, `isScrollLock`, `isShift`, `isWin`

### Methods

`Add`, `AddAction`, `AddChar`, `AddClipboardData`, `AddKey`, `AddKey`, `AddKeys`, `AddRepeat`, `AddSleep`, `AddText`, `AddText`, `SendNow`, `getMod`, `isMod`, `isPressed`, `send`, `sendL`, `sendt`, `waitForHotkey`, `waitForHotkeys`, `waitForKey`, `waitForKey`, `waitForKey`, `waitForKeys`, `waitForNoModifierKeys`, `waitForNoModifierKeysAndMouseButtons`, `waitForReleased`, `waitForReleased`

### Events

`Pasting`