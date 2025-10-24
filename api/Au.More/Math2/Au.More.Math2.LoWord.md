# Method `Au.More.Math2.LoWord`

Gets bits 1-16 as `ushort`. Like C macro `LOWORD`.

```
public static ushort LoWord(nint x)
```

##### Parameters

- *x*  (`nint`)

##### Returns

`ushort`

#### Remarks

The parameter is interpreted as `uint`. The parameter type `nint` allows to avoid explicit cast from `int` and `IntPtr`.