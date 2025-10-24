# Struct `Au.More.Dpi.AwarenessContext`

Can be used to temporarily change thread's DPI awareness context with API `SetThreadDpiAwarenessContext`. Does nothing if the API is unavailable (added in Windows 10 version 1607).

```
public struct Dpi.AwarenessContext : IDisposable
```

##### Remarks

Programs that use this library should use manifest with `dpiAwareness = PerMonitorV2` and `dpiAware = True/PM`. Then default DPI awareness context is `DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2`.

##### Examples

```
using var dac = new Dpi.AwarenessContext(-1);
```

### Constructors

`AwarenessContext(wnd)`, `AwarenessContext(nint)`

### Properties

`Available`

### Methods

`Dispose`