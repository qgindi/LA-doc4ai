# Property `Au.perf.shared`

Gets a reference to a `Au.perf.Instance` variable in shared memory.

```
public static ref perf.Instance shared { get; }
```

##### Property Value

`Au.perf`.`Au.perf.Instance`

#### Remarks

The variable can be used by multiple processes, for example to measure process startup time. Note: slow first time in process, eg 3 ms. It's because need to JIT-compile functions and open shared memory.

#### Examples

```
ref var p = ref perf.shared;
p.First();
//or
perf.shared.First();
```