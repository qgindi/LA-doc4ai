# Method `Au.Types.Pidl.Detach`

Gets the `ITEMIDLIST` and clears this variable so that it cannot be used and will not free the `ITEMIDLIST` memory. To free it use `System.Runtime.InteropServices.Marshal.FreeCoTaskMem`.

```
public nint Detach()
```

##### Returns

`nint`