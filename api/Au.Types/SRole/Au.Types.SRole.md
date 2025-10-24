# Enum `Au.Types.SRole`

`Au.script.role`.

```
public enum SRole
```

### Fields

| Name | Description |
| --- | --- |
| EditorExtension | The task runs in editor process. |
| ExeProgram | The task runs as normal `.exe` program. It can be started from editor or not. It can run on computers where editor not installed. |
| MiniProgram | The task runs in `Au.Task-x64.exe` or `Au.Task-arm.exe` process, started from editor. |