# Property `Au.Types.Pidl.HandleRef`

Gets the `ITEMIDLIST*`.

```
public HandleRef HandleRef { get; }
```

##### Property Value

`HandleRef`

#### Remarks

Use to pass to API where the parameter type is `System.Runtime.InteropServices.HandleRef`. It is safer than `Au.Types.Pidl.UnsafePtr` because ensures that this variable will not be GC-collected during API call even if not referenced after the call.