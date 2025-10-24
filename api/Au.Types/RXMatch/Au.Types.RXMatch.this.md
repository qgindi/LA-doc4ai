# Indexer of `Au.Types.RXMatch`

## Overload 1

Gets group info. Index 0 is whole match. Index 1 is the first group.

```
public ref RXGroup this[int group] { get; }
```

##### Parameters

- *group*  (`int`):
    1-based group index, or 0 for whole match.

##### Exceptions

- `IndexOutOfRangeException`:
    Invalid *group*. Max valid value is `Au.Types.RXMatch.GroupCountPlusOne`.

##### Property Value

`Au.Types.RXGroup`

* * *

## Overload 2

Gets group info of a named group.

```
public ref RXGroup this[string groupName] { get; }
```

##### Parameters

- *groupName*  (`string`):
    Group name. In regular expression, to set name of group `(text)`, use `(?<NAME>text)`.

##### Exceptions

- `ArgumentException`:
    Unknown group name.

##### Property Value

`Au.Types.RXGroup`

#### Remarks

If multiple groups have this name, prefers the first group that matched (`Au.Types.RXGroup.Exists` is `true`).