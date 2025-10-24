# Indexer of `Au.Types.WProp`

## Overload 1

Gets a window property. Calls API `GetProp` and returns its return value.

```
public nint this[string name] { get; }
```

##### Parameters

- *name*  (`string`):
    Property name.

##### Property Value

`nint`

#### Remarks

Supports `Au.lastError`.

* * *

## Overload 2

Gets a window property. Calls API `GetProp` and returns its return value.

```
public nint this[ushort atom] { get; }
```

##### Parameters

- *atom*  (`ushort`):
    Property name atom in the global atom table.

##### Property Value

`nint`

#### Remarks

This overload uses atom instead of string. It's about 3 times faster. See API `GlobalAddAtom`, `GlobalDeleteAtom`.