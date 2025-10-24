# Constructor of `Au.Types.Pidl`

## Overload 1

Assigns an `ITEMIDLIST` to this variable.

```
public Pidl(nint pidl)
```

##### Parameters

- *pidl*  (`nint`):
    `ITEMIDLIST*`. It can be created by any API that creates `ITEMIDLIST`. They allocate the memory with API `CoTaskMemAlloc`. This variable will finally free it with `System.Runtime.InteropServices.Marshal.FreeCoTaskMem` which calls API `CoTaskMemFree`.

* * *

## Overload 2

Combines two `ITEMIDLIST` (parent and child) and assigns the result to this variable.

```
public Pidl(nint pidlAbsolute, nint pidlRelative)
```

##### Parameters

- *pidlAbsolute*  (`nint`):
    Absolute `ITEMIDLIST*` (parent folder).
- *pidlRelative*  (`nint`):
    Relative `ITEMIDLIST*` (child object).

#### Remarks

Does not free *pidlAbsolute* and *pidlRelative*.