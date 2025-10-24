# Class `Au.icon`

Gets icons from/of files etc. Contains native icon handle.

```
public class icon : IDisposable
```

##### Remarks

Native icons must be destroyed. An `icon` variable destroys its native icon when disposing. To dispose, call `Au.icon.Dispose` or use `using` statement. Or use functions like `Au.icon.ToGdipBitmap`, `Au.icon.ToWpfImage`; by default they dispose the `Au.icon` variable. It's OK to not dispose if you use few icons; GC will do it.

##### Inheritance

`object` → `icon`

### Constructors

`icon(nint)`

### Properties

`Handle`, `Size`, `debugSpeed`

### Methods

`Detach`, `Dispose`, `Dispose`, `SetWindowIcon`, `ToGdipBitmap`, `ToGdipIcon`, `ToWpfImage`, `create`, `load`, `of`, `ofPidl`, `ofThisApp`, `ofWindow`, `parsePathIndex`, `stock`, `trayIcon`, `trayIcon`, `winStoreAppImage`, `winStoreAppImage`

### Operators

`implicit operator nint(icon)`