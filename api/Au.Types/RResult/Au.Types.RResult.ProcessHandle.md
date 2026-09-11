# Property `Au.Types.RResult.ProcessHandle`

If used flag `NeedProcessHandle`, contains process handle. Later the `System.Threading.WaitHandle` variable must be disposed.

```csharp
public WaitHandle ProcessHandle { get; }
```

##### Property Value

`WaitHandle`

`null` if no flag or if did not start new process (eg opened the document in an existing process) or if cannot get it.

#### Examples

This code does the same as `run.it(@"mspaint.exe", flags: SRFlags.WaitForExit);`

```csharp
var r = run.it(@"mspaint.exe", flags: SRFlags.NeedProcessHandle);
using(var h = r.ProcessHandle) h?.WaitOne();
```