# Method `Au.script.debug`

Attaches the LibreAutomate's debugger to this process, or waits for a debugger attached to this process. Does nothing if a debugger is already attached.

```
public static void debug(bool showDialog = false)
```

##### Parameters

- *showDialog*  (`bool`):
    Show dialog with process name and id. If `false`, attaches the LA debugger.

#### Remarks

When debugger is attached, this function returns and the script continues to run. The step mode begins when the script encounters one of:

- breakpoint (set in the debugger's IDE).
- exception.
- clicked **Pause** button in IDE.
- `System.Diagnostics.Debugger.Break`, `System.Diagnostics.Debug.Assert` etc.

If *showDialog* is `false` and LibreAutomate is running, attaches the LA debugger. Cannot attach if it's busy (debugging).

Some other programs that have a .NET debugger:

- Visual Studio. It's the best, but huge (~10 GB). The community edition is free. Use menu **Debug > Attach to process**.
- Visual Studio Code. It's much smaller. Free.
- JetBrains Rider.

> **Note:**
> If the script process is running as administrator, the debugger process must run as administrator too.

> **Note:**
> When attaching an external debugger (Visual Studio etc), make sure it debugs .NET code, not native code etc.

See also [Debugging C# scripts](../editor/Debugger.html).