# Method `Au.More.Math2.LoShort`

Gets bits 1-16 as `short`. Like C macro `GET_X_LPARAM`.

```
public static short LoShort(nint x)
```

##### Parameters

- *x*  (`nint`)

##### Returns

`short`

#### Remarks

The parameter is interpreted as `uint`. The parameter type `nint` allows to avoid explicit cast from `int` and `IntPtr`.