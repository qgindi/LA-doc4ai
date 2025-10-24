# Method `Au.wpfBuilder.Margin`

## Overload 1

Sets margin of the last added element.

```
public wpfBuilder Margin(Thickness margin)
```

##### Parameters

- *margin*  (`Thickness`)

##### Returns

`Au.wpfBuilder`

* * *

## Overload 2

Sets margin of the last added element.

```
public wpfBuilder Margin(double? left = null, double? top = null, double? right = null, double? bottom = null)
```

##### Parameters

- *left*  (`double?`)
- *top*  (`double?`)
- *right*  (`double?`)
- *bottom*  (`double?`)

##### Returns

`Au.wpfBuilder`

* * *

## Overload 3

Sets margin of the last added element.

```
public wpfBuilder Margin(string margin)
```

##### Parameters

- *margin*  (`string`):
    String containing uppercase or lowercase letters for margin sides (`L`, `T`, `R`, `B`) optionally followed by a number (default 0) and optionally separated by spaces. Or just single number, to set all sides equal. Examples: `"tb"` (top 0, bottom 0), `"L5 R15"` (left 5, right 15), `"2"` (all sides 2).

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `ArgumentException`:
    Invalid string.