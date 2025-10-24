# Method `Au.More.Math2.PercentFromValue`

## Overload 1

Calculates how many % of *whole* is *part*: `100L * part / whole`.

```
public static int PercentFromValue(int whole, int part, bool canRoundUp = false)
```

##### Parameters

- *whole*  (`int`)
- *part*  (`int`)
- *canRoundUp*  (`bool`):
    Round down or up. If `false` (default), can only round down.

##### Returns

`int`

##### Exceptions

- `OverflowException`

* * *

## Overload 2

Calculates how many % of *whole* is *part*: `100 * part / whole`.

```
public static double PercentFromValue(double whole, double part)
```

##### Parameters

- *whole*  (`double`)
- *part*  (`double`)

##### Returns

`double`