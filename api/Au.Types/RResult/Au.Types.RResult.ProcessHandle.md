# Property `Au.Types.RResult.ProcessHandle`

If used flag `NeedProcessHandle`, contains process handle. Later the `System.Threading.WaitHandle` variable must be disposed.

```
public WaitHandle ProcessHandle { get; }
```

##### Property Value

`WaitHandle`

`null` if no flag or if did not start new process (eg opened the document in an existing process) or if cannot get it.

#### Examples

This code does the same as `run.it(@"notepad.exe", flags: SRFlags.WaitForExit);`

```
var r = run.it(@"notepad.exe", flags: SRFlags.NeedProcessHandle);
using(var h = r.ProcessHandle) h?.WaitOne();
```