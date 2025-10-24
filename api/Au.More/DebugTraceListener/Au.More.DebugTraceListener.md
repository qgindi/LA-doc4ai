# Class `Au.More.DebugTraceListener`

Replaces the default trace listener with a listener that shows a message box on a failed assertion.

```
public class DebugTraceListener : DefaultTraceListener, IDisposable
```

##### Remarks

The new trace listener overrides the `System.Diagnostics.DefaultTraceListener.Fail` method. On failed assertion (`System.Diagnostics.Debug.Assert`, `System.Diagnostics.Trace.Assert`, `System.Diagnostics.Debug.Fail`, `System.Diagnostics.Trace.Fail`) it shows a message box with buttons **Exit** **Debug** **Ignore**, unless debugger is attached or `System.Diagnostics.DefaultTraceListener.AssertUiEnabled` is `false`.

##### Inheritance

`object` → `MarshalByRefObject` → `TraceListener` → `DefaultTraceListener` → `DebugTraceListener`

### Methods

`Fail`, `Setup`