# Class `Au.Types.Pidl`

Manages an `ITEMIDLIST` structure that is used to identify files and other shell objects instead of a file-system path.

```
public class Pidl : IDisposable
```

##### Remarks

Wraps an `ITEMIDLIST*`, also known as *PIDL* or `LPITEMIDLIST`.

When calling native shell API, virtual objects can be identified only by `ITEMIDLIST*`. Some API also support "parsing name", which may look like `"::{CLSID-1}\::{CLSID-2}"`. File-system objects can be identified by path as well as by `ITEMIDLIST*`. URLs can be identified by URL as well as by `ITEMIDLIST*`.

The `ITEMIDLIST` structure is in unmanaged memory. You can dispose `Pidl` variables, or GC will do it later. Always dispose if creating many.

This class has only `ITEMIDLIST` functions that are used in this library. Look for other functions on the Internet. Many of them are named with IL prefix, like `ILClone`, `ILGetSize`, `ILFindLastID`.

##### Inheritance

`object` → `Pidl`

### Constructors

`Pidl(nint)`, `Pidl(nint, nint)`

### Properties

`HandleRef`, `IsNull`, `UnsafePtr`

### Methods

`Detach`, `Dispose`, `Dispose`, `FromString`, `ToHexString`, `ToHexString`, `ToShellString`, `ToShellString`, `ToString`, `ToString`, `ValueEquals`