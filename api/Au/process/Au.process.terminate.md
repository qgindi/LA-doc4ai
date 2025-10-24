# Method `Au.process.terminate`

## Overload 1

Terminates (ends) the specified process.

```
public static bool terminate(int processId, int exitCode = 0)
```

##### Parameters

- *processId*  (`int`):
    Process id.
- *exitCode*  (`int`):
    Process exit code.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

#### Remarks

Uses API `WTSTerminateProcess` or `TerminateProcess`. They are async; usually the process ends after 2 - 200 ms, depending on program etc.

Does not try to end process "softly" (close main window). Unsaved data will be lost.

Alternatives: run `taskkill.exe` or `pskill.exe` (download). See `Au.run.console`. More info on the internet.

#### Examples

Restart the shell process (explorer).

```
process.terminate(wnd.getwnd.shellWindow.ProcessId, 1);
if (!dialog.showYesNo("Restart explorer?")) return;
run.it(folders.Windows + @"explorer.exe", flags: RFlags.InheritAdmin);
```

* * *

## Overload 2

Terminates (ends) all processes of the specified program or programs.

```
public static int terminate(string processName, bool allSessions = false, int exitCode = 0)
```

##### Parameters

- *processName*  (`string`):
    Process executable file name (like `"notepad.exe"`) or full path. String format: [wildcard expression](../articles/Wildcard%20expression.html).
- *allSessions*  (`bool`):
    Processes of any user session. If `false` (default), only processes of this user session.
- *exitCode*  (`int`):
    Process exit code.

##### Returns

`int`

The number of successfully terminated processes.

##### Exceptions

- `ArgumentException`:

    - *processName* is `""` or `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).