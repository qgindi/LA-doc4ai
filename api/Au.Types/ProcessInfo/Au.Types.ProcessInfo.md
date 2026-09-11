# Struct `Au.Types.ProcessInfo`

Contains process name (like `"abc.exe"`), id and user session id.

```csharp
public record struct ProcessInfo : IEquatable<ProcessInfo>
```

### Constructors

`ProcessInfo(string, int, int)`

### Properties

`Id`, `Name`, `SessionId`