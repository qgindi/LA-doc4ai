# Method `Au.script.setup`

Adds various features to this script task (running script): tray icon, exit on `Ctrl+Alt+Delete`, etc.

```
public static void setup(bool trayIcon = false, bool sleepExit = false, bool lockExit = false, bool debug = false, UExcept exception = UExcept.Print, KKey exitKey = 0, KKey pauseKey = KKey.ScrollLock, string f_ = null)
```

##### Parameters

- *trayIcon*  (`bool`):
    Add tray icon. See `Au.script.trayIcon`.
- *sleepExit*  (`bool`):
    End this process when computer is going to sleep or hibernate.
- *lockExit*  (`bool`):
    End this process when the active desktop has been switched (PC locked, `Ctrl+Alt+Delete`, screen saver, etc, except UAC consent). Then to end this process you can use hotkeys `Win+L` (lock computer) and `Ctrl+Alt+Delete`. Most mouse, keyboard, clipboard and window functions don't work when other desktop is active. Many of them then throw exception, and the script would end anyway.
- *debug*  (`bool`):
    Call `Au.More.DebugTraceListener.Setup` with *usePrint* `true`. It makes `System.Diagnostics.Debug.Assert` etc useful when not debugging.
- *exception*  (`Au.Types.UExcept`):
    What to do on unhandled exception (event `System.AppDomain.UnhandledException`).
- *exitKey*  (`Au.Types.KKey`):

    If not 0, the script task will end when this key pressed. Will call `System.Environment.Exit`. Example: `exitKey: KKey.MediaStop`.

    Recommended keys: media, volume, browser and applaunch keys. They work even when the process of the active window is admin (UAC) and this script isn't. In any case, the key does not work if somewhere used for a global hotkey, trigger, *exitKey* or *pauseKey*. Also the key does not work when at that time a modifier key is pressed by a script; it also can be dangerous because may generate a trigger or hotkey used by an app or OS.
- *pauseKey*  (`Au.Types.KKey`):

    Let `Au.script.pause` pause/resume when this key pressed. Default: `ScrollLock` (`Fn+S`, `Fn+K` or similar). If `CapsLock`, pauses when it is toggled (even if was toggled at startup) and resumes when untoggled.

    `ScrollLock`, `CapsLock` and `NumLock` are the most reliable. Other keys have the same problems as with *exitKey*.
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html). Don't use. Or use like `f_: null` to disable script editing via tray icon.

##### Exceptions

- `InvalidOperationException`:
    Already called.

#### Remarks

Tip: in **Options > Templates** you can set default code for new scripts.

If your program was compiled not in LibreAutomate, call this function (maybe with zero arguments) if you want the program behave like if it was compiled with LibreAutomate (invariant culture, `STAThread`, unhandled exception action).

Does nothing if role `editorExtension` or if running in WPF preview mode.