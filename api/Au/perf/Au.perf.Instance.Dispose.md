# Method `Au.perf.Instance.Dispose`

Calls `Au.perf.Instance.NW`, which calls `Au.perf.Instance.Next` and `Au.perf.Instance.Write`.

```
public void Dispose()
```

##### Implements

`IDisposable.Dispose()`

#### Remarks

Don't need to dispose variables of this type. This function just allows to use `using` instead of `Au.perf.Instance.NW`. See example.

If `Au.perf.Instance.Incremental`, calls just `Au.perf.Instance.Write`.

#### Examples

```
using(var p1 = perf.local()) { //p1.First();
	1.ms();
	p1.Next();
	1.ms();
} //p1.NW();
```