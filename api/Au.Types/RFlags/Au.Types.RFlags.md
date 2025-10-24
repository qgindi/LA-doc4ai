# Enum `Au.Types.RFlags`

Flags for `Au.run.it`.

```
[Flags]
public enum RFlags
```

### Fields

| Name | Description |
| --- | --- |
| Admin | (see section `details1` in Footnotes) |
| InheritAdmin | (see section `details2` in Footnotes) |
| MostUsed | Add the app to the "Most used" list in the Start menu if launched often. |
| NeedProcessHandle | If started new process, get process handle (`Au.Types.RResult.ProcessHandle`). |
| ShowErrorUI | Show error message box if fails, for example if file not found. Note: this does not disable exceptions. To avoid exceptions use try/catch or `Au.run.itSafe`. |
| WaitForExit | If started new process, wait until it exits. |

## Footnotes

###### details1

Run new process as administrator. 
If this process isn't admin:

- Shows UAC consent dialog.
- Uses verb `"runas"`, therefore other verb cannot be specified.
- Cannot set current directory for the new process.
- The new process does not inherit environment variables of this process.

###### details2

If this process runs as administrator, run new process as administrator too. 
Without this flag, if this process runs as administrator:

- Starts new process as non-administrator from the shell process (`explorer.exe`).
- If it fails (for example if shell process isn't running), calls `Au.print.warning` and starts new process as administrator.
- The new process does not inherit environment variables of this process.