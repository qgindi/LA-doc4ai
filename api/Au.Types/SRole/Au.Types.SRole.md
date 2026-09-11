# Enum `Au.Types.SRole`

`Au.script.role`.

```csharp
public enum SRole
```

## Fields

### `EditorExtension`

The task runs in editor process.

### `ExeProgram`

The task runs as normal `.exe`program.
It can be started from editor or not. It can run on computers where editor not installed.

### `MiniProgram`

The task runs in `Au.Task.exe` or `Au.Task-arm.exe` process, started from editor.