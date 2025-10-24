# End script task, pause, exit

You can end a running script task in several ways.

1. Click the **End task** toolbar button or menu command.
2. If the script adds a [tray icon](Tray%20icon%20and%20notifications.html), right-click it and select **End task**.
3. If the script calls `Au.script.setup` like this at the start, press the exit key. If UAC blocks it, try with `Alt`, `Ctrl` or `Win`.

```
script.setup(trayIcon: true, exitKey: KKey.MediaStop);
```

1. If the script calls `Au.script.setup` like this at the start, press the `Sleep` button on the keyboard.

```
script.setup(trayIcon: true, sleepExit: true);
```

1. Press `Win+L` or `Ctrl+Alt+Delete`. If the script calls `Au.script.setup` like this at the start, it will end immediately. Else it will end when calling a keyboard or mouse input function or `Au.wnd.Activate`, because these functions then fail and throw exception; some other functions too.

```
script.setup(trayIcon: true, lockExit: true);
```

1. Insert `Au.script.pause` in loops etc, in places safe to pause or end the script. To end the script, press the pause key (default `ScrollLock`), and then use any of the above ways to end the paused script.

```
script.pause();
```

Changing the pause key.

```
script.setup(trayIcon: true, sleepExit: true, pauseKey: KKey.MediaPlayPause);
```

1. A script can call `Au.script.end` to end another script. For example you can add a trigger with this action code.

```
script.end("Script name.cs");
```

1. A script can set a trigger to end itself.

```
using Au.Triggers;

run.thread(() => {
	ActionTriggers Triggers = new();
	Triggers.Hotkey["?+F1"] = o => { script.end(); };
	Triggers.Run();
});

dialog.show("Main script code");
```

See also: [return, exit](return%2C%20goto%20%28exit%2C%20end%2C%20stop%2C%20jump%29.html), [throw exception](Errors%2C%20exceptions%2C%20try-catch-finally%2C%20throw.html).