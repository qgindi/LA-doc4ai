# Method `Au.More.Math2.PercentToValue`

## Overload 1

Returns *percent* % of *whole*: `(long)whole * percent / 100`.

```
public static int PercentToValue(int whole, int percent, bool canRoundUp = false)
```

##### Parameters

- *whole*  (`int`)
- *percent*  (`int`)
- *canRoundUp*  (`bool`):
    Use `Au.More.Math2.MulDiv`, which can round down or up. If `false` (default), can only round down.

##### Returns

`int`

##### Exceptions

- `OverflowException`

* * *

## Overload 2

Returns *percent* % of *whole*: `whole * percent / 100`.

```
public static double PercentToValue(double whole, double percent)
```

##### Parameters

- *whole*  (`double`)
- *percent*  (`double`)

##### Returns

`double`