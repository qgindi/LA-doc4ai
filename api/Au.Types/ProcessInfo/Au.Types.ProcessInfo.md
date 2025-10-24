# Struct `Au.Types.ProcessInfo`

Contains process name (like `"notepad.exe"`), id and user session id.

```
public record struct ProcessInfo : IEquatable<ProcessInfo>
```

### Constructors

`ProcessInfo(string, int, int)`

### Properties

`Id`, `Name`, `SessionId`