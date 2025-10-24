# Property `Au.print.isWritingToConsole`

Returns `true` if is writing to console, `false` if to the output window etc.

```
public static bool isWritingToConsole { get; }
```

##### Property Value

`bool`

#### Remarks

Does not write to console in these cases:

- `Au.print.isConsoleProcess` is `false`.
- `Au.print.ignoreConsole` is `true`.
- `Au.print.logFile` is not `null`.
- The startup info of this process tells to not show console window and to not redirect the standard output.