# Method `Au.More.ScriptEditor.Open`

Opens a script or other file. Also can move the text cursor. Does nothing if editor isn't running.

```
public static void Open(string file, int? line = null, int? offset = null)
```

##### Parameters

- *file*  (`string`):
    A file in current workspace. Can be full path, or relative path in workspace, or file name with extension (`".cs"` etc). If folder, selects it.
- *line*  (`int?`):
    If not `null`, goes to this 1-based line index.
- *offset*  (`int?`):
    If not `null`, goes to this 0-based column index in line (if *line* not `null`) or to this 0-based position in text (if *line* `null`).