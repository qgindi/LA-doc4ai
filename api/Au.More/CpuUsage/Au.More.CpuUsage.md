# Class `Au.More.CpuUsage`

Gets CPU usage.

```csharp
public sealed class CpuUsage : IDisposable
```

##### Remarks

You can use the static functions (easier) or a `CpuUsage` instance. A `CpuUsage` instance must be disposed (use `using`).

##### Examples

```csharp
using var u = new CpuUsage(); //all processes
//using var u = new CpuUsage(process.getProcessId("Au.Editor.exe")); //single process
//using var u = new CpuUsage(process.getProcessIds("chrome.exe")); //all Chrome processes
for (; ; ) {
	if (!u.Start()) break;
	Thread.Sleep(500);
	print.it(u.Stop());
}
```

##### Inheritance

`object` → `CpuUsage`

### Constructors

`CpuUsage()`, `CpuUsage(IEnumerable<int>)`, `CpuUsage(int)`

### Properties

`ProcessorCount`

### Methods

`Dispose`, `OfAllProcesses`, `OfProcess`, `OfProcesses`, `Start`, `Stop`