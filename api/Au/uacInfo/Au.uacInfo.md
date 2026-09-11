# Class `Au.uacInfo`

Gets [UAC](🔗) integrity level and other security info of this and other processes.

```csharp
public sealed class uacInfo : IDisposable
```

##### Remarks

An `uacInfo` variable contains a process access token handle that is used to get security info. Always dispose `uacInfo` variables to close the handle.

##### Inheritance

`object` → `uacInfo`

### Properties

`Elevation`, `Failed`, `IntegrityLevel`, `IsUIAccess`, `UnsafeTokenHandle`, `isAdmin`, `isUacDisabled`, `ofThisProcess`

### Methods

`Dispose`, `ofProcess`