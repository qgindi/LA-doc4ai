# Struct `Au.Types.WOwner`

Used with `Au.wnd.find`and similar functions to specify an owner of the window.
Can be program name (like`"abc.exe"`), process id (`Au.Types.WOwner.Process`), thread id (`Au.Types.WOwner.Thread` or `Au.Types.WOwner.ThisThread`), owner window.

```csharp
public struct WOwner
```

### Properties

`IsEmpty`, `ThisThread`

### Methods

`GetValue`, `Process`, `Thread`

### Operators

`implicit operator WOwner(wnd)`, `implicit operator WOwner(string)`