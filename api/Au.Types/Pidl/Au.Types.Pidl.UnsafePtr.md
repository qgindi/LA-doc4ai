# Property `Au.Types.Pidl.UnsafePtr`

Gets the `ITEMIDLIST*`.

```
public nint UnsafePtr { get; }
```

##### Property Value

`nint`

#### Remarks

The `ITEMIDLIST` memory is managed by this variable and will be freed when disposing or GC-collecting it. Use `System.GC.KeepAlive` where need.