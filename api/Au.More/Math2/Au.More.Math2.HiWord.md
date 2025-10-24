# Method `Au.More.Math2.HiWord`

Gets bits 17-32 as `ushort`. Like C macro `HIWORD`.

```
public static ushort HiWord(nint x)
```

##### Parameters

- *x*  (`nint`)

##### Returns

`ushort`

#### Remarks

The parameter is interpreted as `uint`. The parameter type `nint` allows to avoid explicit cast from `int` and `IntPtr`.