# Method `Au.More.Math2.HiShort`

Gets bits 17-32 as `short`. Like C macro `GET_Y_LPARAM`.

```
public static short HiShort(nint x)
```

##### Parameters

- *x*  (`nint`)

##### Returns

`short`

#### Remarks

The parameter is interpreted as `uint`. The parameter type `nint` allows to avoid explicit cast from `int` and `IntPtr`.