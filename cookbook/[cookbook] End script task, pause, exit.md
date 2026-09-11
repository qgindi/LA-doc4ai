# End script task, pause, exit

You can end a running script task in several ways.

1. Click the **End task** toolbar button or menu command.
2. If the script adds a [tray icon](🔗), right-click it and select **End task**.
3. If the script calls `Au.script.setup` like this at the start, press the exit key. If UAC blocks it, try with `Alt`, `Ctrl` or `Win`.

```csharp
script.setup(trayIcon: true, exitKey: KKey.MediaStop);
```

1. If the script calls `Au.script.setup` like this at the start, press the `Sleep` button on the keyboard.

```csharp
script.setup(trayIcon: true, sleepExit: true);
```

1. Press `Win+L` or `Ctrl+Alt+Delete`. If the script calls `Au.script.setup` like this at the start, it will end immediately. Else it will end when calling a keyboard or mouse input function or `Au.wnd.Activate`, because these functions then fail and throw exception; some other functions too.

```csharp
script.setup(trayIcon: true, lockExit: true);
```

1. Insert `Au.script.pause` in loops etc, in places safe to pause or end the script. To end the script, press the pause key (default `ScrollLock`), and then use any of the above ways to end the paused script.

```csharp
script.pause();
```

Changing the pause key.

```csharp
script.setup(trayIcon: true, sleepExit: true, pauseKey: KKey.MediaPlayPause);
```

1. A script can call `Au.script.end` to end another script. For example you can add a trigger with this action code.

```csharp
script.end("Script name.cs");
```

1. A script can set a trigger to end itself.

```csharp
using Au.Triggers;

run.thread(() => {
	ActionTriggers Triggers = new();
	Triggers.Hotkey["?+F1"] = o => { script.end(); };
	Triggers.Run();
});

dialog.show("Main script code");
```

See also: [return, exit](🔗), [throw exception](🔗).