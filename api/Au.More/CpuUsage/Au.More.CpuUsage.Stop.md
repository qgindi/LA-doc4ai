# Method `Au.More.CpuUsage.Stop`

Ends measuring CPU usage, and gets result. Call this after calling `Au.More.CpuUsage.Start` and waiting at least 1 ms. Don't call if `Start` returned `false`.

```
public double Stop()
```

##### Returns

`double`

CPU usage 0 to 100 %.

##### Exceptions

- `InvalidOperationException`:
    Called without successful `Au.More.CpuUsage.Start`.