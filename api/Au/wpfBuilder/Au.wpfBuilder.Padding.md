# Method `Au.wpfBuilder.Padding`

## Overload 1

Sets padding of the last added control.

```
public wpfBuilder Padding(Thickness thickness)
```

##### Parameters

- *thickness*  (`Thickness`)

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    The last added element does not have `Padding` property.

* * *

## Overload 2

Sets padding of the last added control.

```
public wpfBuilder Padding(double? left = null, double? top = null, double? right = null, double? bottom = null)
```

##### Parameters

- *left*  (`double?`)
- *top*  (`double?`)
- *right*  (`double?`)
- *bottom*  (`double?`)

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    The last added element does not have `Padding` property.

* * *

## Overload 3

Sets padding of the last added control.

```
public wpfBuilder Padding(string padding)
```

##### Parameters

- *padding*  (`string`):
    String containing uppercase or lowercase letters for padding sides (`L`, `T`, `R`, `B`) optionally followed by a number (default 0) and optionally separated by spaces. Or just single number, to set all sides equal. Examples: `"tb"` (top 0, bottom 0), `"L5 R15"` (left 5, right 15), `"2"` (all sides 2).

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    The last added element does not have `Padding` property.
- `ArgumentException`:
    Invalid string.