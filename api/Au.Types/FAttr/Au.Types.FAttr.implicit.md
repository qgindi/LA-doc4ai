# Operator `Au.Types.FAttr.implicit operator`

## Overload 1

Returns `Au.Types.FAttr.Exists`.

```
public static implicit operator bool(FAttr fa)
```

##### Parameters

- *fa*  (`Au.Types.FAttr`)

##### Returns

`bool`

* * *

## Overload 2

Returns 0 if !`Au.Types.FAttr.Exists`, 1 if `Au.Types.FAttr.File`, 2 if `Au.Types.FAttr.Directory`. Can be used with switch.

```
public static implicit operator int(FAttr fa)
```

##### Parameters

- *fa*  (`Au.Types.FAttr`)

##### Returns

`int`