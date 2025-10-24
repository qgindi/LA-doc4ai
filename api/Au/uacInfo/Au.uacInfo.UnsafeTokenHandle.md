# Property `Au.uacInfo.UnsafeTokenHandle`

The access token handle.

```
public nint UnsafeTokenHandle { get; }
```

##### Property Value

`nint`

#### Remarks

The handle is managed by this variable and will be closed when disposing or GC-collecting it. Use `System.GC.KeepAlive` where need.