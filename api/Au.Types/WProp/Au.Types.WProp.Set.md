# Method `Au.Types.WProp.Set`

## Overload 1

Sets a window property. Calls API `SetProp` and returns its return value.

```
public bool Set(string name, nint value)
```

##### Parameters

- *name*  (`string`):
    Property name.
- *value*  (`nint`):
    Property value.

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.

Later call `Au.Types.WProp.Remove` to remove the property. If you use many unique property names and don't remove the properties, the property name strings can fill the global atom table which is of a fixed size (about 48000) and which is used by all processes for various purposes.

* * *

## Overload 2

Sets a window property. Calls API `SetProp` and returns its return value.

```
public bool Set(ushort atom, nint value)
```

##### Parameters

- *atom*  (`ushort`):
    Property name atom in the global atom table.
- *value*  (`nint`):
    Property value.

##### Returns

`bool`

#### Remarks

This overload uses atom instead of string. It's about 3 times faster. See API `GlobalAddAtom`, `GlobalDeleteAtom`.