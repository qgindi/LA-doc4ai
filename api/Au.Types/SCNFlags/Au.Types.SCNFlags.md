# Enum `Au.Types.SCNFlags`

Flags for `Au.filesystem.more.notifyShell`.

```csharp
[Flags]
public enum SCNFlags
```

##### Remarks

The names are as in API `SHChangeNotify` documentation but without prefix `SHCNF_`.

## Fields

### `SHCNF_FLUSH`

Let Explorer process the notification without a delay. Wait until finished.

### `SHCNF_FLUSHNOWAIT`

Let Explorer process the notification without a delay. Don't wait until finished.

### `SHCNF_NOTIFYRECURSIVE`