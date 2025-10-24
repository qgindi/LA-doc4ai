# Method `Au.Types.RXMatch.GroupNumberFromName`

## Overload 1

Finds a named group and returns its 1-based index. Returns -1 if not found.

```
public int GroupNumberFromName(string groupName)
```

##### Parameters

- *groupName*  (`string`):
    Group name. In regular expression, to set name of group `(text)`, use `(?<NAME>text)`.

##### Returns

`int`

##### Exceptions

- `ArgumentNullException`

#### Remarks

If multiple groups have this name, prefers the first group that matched (`Au.Types.RXGroup.Exists` is `true`).

### See Also

`Au.regexp.GetGroupNumberOf`

* * *

## Overload 2

Finds a named group and returns its 1-based index. Returns -1 if not found.

```
public int GroupNumberFromName(string groupName, out bool notUnique)
```

##### Parameters

- *groupName*  (`string`):
    Group name. In regular expression, to set name of group `(text)`, use `(?<NAME>text)`.
- *notUnique*  (`bool`):
    Receives `true` if multiple groups have this name.

##### Returns

`int`

##### Exceptions

- `ArgumentNullException`

#### Remarks

If multiple groups have this name, prefers the first group that matched (`Au.Types.RXGroup.Exists` is `true`).

### See Also

`Au.regexp.GetGroupNumberOf`