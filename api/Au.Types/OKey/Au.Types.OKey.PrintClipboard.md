# Method `Au.Types.OKey.PrintClipboard`

Writes to the output some info about current clipboard data.

```
public static void PrintClipboard()
```

#### Remarks

Shows this info for each clipboard format: format name, time spent to get data (microseconds), data size (bytes), and whether this format would be restored (depends on `Au.Types.OKey.RestoreClipboardExceptFormats`).

> **Note:**
> Copy something to the clipboard each time before calling this function. Don't use `Au.clipboard.copy` and don't call this function in loop. Else it shows small times.

The time depends on app, etc. More info: `Au.Types.OKey.RestoreClipboardExceptFormats`.

#### Examples

```
OKey.PrintClipboard();
```