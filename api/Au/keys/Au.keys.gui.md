# Class `Au.keys.gui`

Gets key states for using in UI code (winforms, WPF, etc).

```
public static class keys.gui
```

##### Remarks

Use functions of this class in user interface code (winforms, WPF, etc). In other code (automation scripts, etc) usually it's better to use functions of `Au.keys` class.

In Windows there are two API to get key state - `GetKeyState` and `GetAsyncKeyState`.

API `GetAsyncKeyState` is used by class `Au.keys` and not by this class (`keys.gui`). When physical key state changes (pressed/released), `GetAsyncKeyState` sees the change immediately. It is good in automation scripts, but not good in UI code because the state is not synchronized with the message queue.

This class (`keys.gui`) uses API `GetKeyState`. In the foreground thread (of the active window), it sees key state changes not immediately but after the thread reads key messages from its queue. It is good in UI threads. In background threads this API usually works like `GetAsyncKeyState`, but it depends on API `AttachThreadInput` and in some cases is less reliable, for example may be unaware of keys pressed before the thread started.

The key state returned by these API is not always the same as of the physical keyboard. There is no API to get real physical state. Some cases when it is different:

1. The key is pressed or released by software, such as the `Au.keys.send` function of this library.
2. The key is blocked by a low-level hook. For example, hotkey triggers of this library use hooks.
3. The foreground window belongs to a process with higher UAC integrity level.

Also there is API `GetKeyboardState`. It gets states of all keys in single call. Works like `GetKeyState`.

##### Inheritance

`object` → `keys.gui`

### Properties

`isAlt`, `isCapsLock`, `isCtrl`, `isNumLock`, `isScrollLock`, `isShift`, `isWin`

### Methods

`getKeyState`, `getMod`, `isMod`, `isPressed`, `isToggled`