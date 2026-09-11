# Enum `Au.Types.WHFlags`

Flags for `Au.wait.forHandle`

```csharp
[Flags]
public enum WHFlags
```

## Fields

### `All`

Wait until all handles are signaled.

### `DoEvents`

While waiting, dispatch Windows messages, events, hooks etc. Like `Au.wait.doEvents`.