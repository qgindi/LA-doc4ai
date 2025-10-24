# Method `Au.Types.WProp.Remove`

## Overload 1

Removes a window property. Calls API `RemoveProp` and returns its return value.

```
public nint Remove(string name)
```

##### Parameters

- *name*  (`string`):
    Property name. Other overload allows to use global atom instead, which is faster.

##### Returns

`nint`

#### Remarks

Supports `Au.lastError`.

* * *

## Overload 2

Removes a window property. Calls API `RemoveProp` and returns its return value.

```
public nint Remove(ushort atom)
```

##### Parameters

- *atom*  (`ushort`):
    Property name atom in the global atom table.

##### Returns

`nint`