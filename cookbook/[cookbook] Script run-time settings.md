# Script run-time settings

The **Properties** dialog contains only settings for compiling and launching the script. Run-time settings can be set in script code.

Function `Au.script.setup` can add [tray icon](Tray%20icon%20and%20notifications.html), several ways to terminate the script process, and more.

```
script.setup(trayIcon: true, sleepExit: true);
```

The **ifRunning** option isn't applied if the `.exe` script is launched not from the editor. Then function `Au.script.single` can be used to ensure single process instance.

```
script.single("mutex7654329");
```

Use localized string and date parsing, formatting, comparing, display, etc.

```
process.thisProcessCultureIsInvariant = false;
```

Class `Au.dialog.options` can be used to set some options for standard dialogs.

```
dialog.options.defaultScreen = screen.ofMouse;
2.s();
dialog.show("");
```

Use class `Au.opt` to set options for mouse, keyboard, clipboard and some other functions.

```
opt.mouse.MoveSpeed = 30;
opt.key.TextSpeed = 50;

var w = wnd.find(1, "*- Notepad", "Notepad");
mouse.click(w, .5f, .5f);
keys.sendt("Slow text");
```

Class `Au.print` has several options.

```
print.redirectDebugOutput = true;
// ...
Debug.Print("debug");
```