# Struct `Au.perf.Instance`

Performs time measurements and stores measurement data.

```
public struct perf.Instance : IDisposable
```

##### Remarks

Static functions of `Au.perf` class use a single static variable of this type to perform measurements. Use a variable of this type instead when you want to have multiple independent measurements. See `Au.perf.local`. Variables of this type usually are used as local (in single function), but also can be used anywhere (class fields, unmanaged memory). This type is a struct (value type), and not small (184 bytes). Don't use it as a function parameter without ref. To share a variable between functions use a field in your class. Don't need to dispose variables of this type. The `Au.perf.Instance.Dispose` function just calls `Au.perf.Instance.NW`.

### Properties

`Incremental`, `TimeTotal`

### Methods

`Dispose`, `First`, `NW`, `Next`, `ToArray`, `ToString`, `Write`