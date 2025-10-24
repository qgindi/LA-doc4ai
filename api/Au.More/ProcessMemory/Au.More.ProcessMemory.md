# Class `Au.More.ProcessMemory`

Allocates, writes and reads memory in other process.

```
public class ProcessMemory : IDisposable
```

##### Remarks

Must be disposed. Example: `using(var pm=new ProcessMemory(...)) { ... }`.

##### Inheritance

`object` → `ProcessMemory`

### Constructors

`ProcessMemory(wnd, int, bool)`, `ProcessMemory(int, int, bool)`

### Properties

`Mem`, `MemAllocated`, `ProcessHandle`

### Methods

`Dispose`, `Dispose`, `Read`, `Read`, `ReadByteString`, `ReadCharString`, `Write`, `Write`, `WriteByteString`, `WriteCharString`