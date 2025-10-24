# Enum `Au.Types.UExcept`

Flags for `Au.script.setup` parameter *exception*. Defines what to do on unhandled exception. Default is `Print`, even if `script.setup` not called (with default compiler only).

```
[Flags]
public enum UExcept
```

### Fields

| Name | Description |
| --- | --- |
| Dialog | Show dialog with exception info. If editor available, the dialog contains links to functions in the call stack. To close the dialog when a link clicked, add flag `Print`. |
| Print | Display exception info in output. |