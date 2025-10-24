# Method `Au.miscInfo.isInputDesktop`

Returns `true` if current thread is on the input desktop and therefore can use mouse, keyboard, clipboard and window functions.

```
public static bool isInputDesktop(bool detectLocked = false)
```

##### Parameters

- *detectLocked*  (`bool`):
    Return `false` if the active window is a full-screen window of `LockApp.exe` on Windows 10+. For example when computer has been locked but still not displaying the password field. Slower.

##### Returns

`bool`

#### Remarks

Usually this app is running on default desktop. Examples of other desktops: the `Ctrl+Alt+Delete` screen, the PC locked screen, screen saver, UAC consent, custom desktops. If one of these is active, this process cannot use many mouse, keyboard, clipboard and window functions. They either throw exception or do nothing.

### See Also

`Au.Types.InputDesktopException`