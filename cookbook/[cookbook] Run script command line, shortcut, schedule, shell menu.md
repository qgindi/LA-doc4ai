# Run script command line, shortcut, schedule, shell menu

Other programs can launch scripts in two ways.

1. Let the editor program launch the script. [More info](/editor/Command%20line.html). Command line examples:

    `Au.Editor.exe Script5.cs` `Au.Editor.exe \Folder\Script5.cs` `Au.Editor.exe "Script name.cs" /argument1 "argument 2"` `Au.Editor.exe *Script5.cs`

    With `*` the program can wait until the script ends and capture text written with `Au.script.writeResult`.

    To create a command line string to run current script, use menu **TT > Script launchers**. Also there you'll find tools to create Windows Task Scheduler tasks (triggers: date/time, event log, startup, session connect/disconnect/lock/unlock, idle), shortcuts and [shell context menu items](https://www.libreautomate.com/forum/showthread.php?tid=7819).
2. Run the script without the editor. For it need to [create .exe program](/editor/Publish.html) from the script. Then launch it like any other program. Example:

    `C:\Test\Script5.exe`

    Note: the **ifRunning** and **uac** options then aren't applied. To ensure single running instance, use `Au.script.single`.