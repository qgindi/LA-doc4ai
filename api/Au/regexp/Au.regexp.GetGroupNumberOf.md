# Method `Au.regexp.GetGroupNumberOf`

Finds a named group and returns its 1-based index. Returns -1 if not found.

```
public int GetGroupNumberOf(string groupName)
```

##### Parameters

- *groupName*  (`string`):
    Group name. In regular expression, to set name of group `(text)`, use `(?<NAME>text)`.

##### Returns

`int`

##### Exceptions

- `ArgumentNullException`
- `ArgumentException`:
    Multiple groups have this name.

### See Also

`Au.Types.RXMatch.GroupNumberFromName`

`Au.Types.RXMatch.GroupNumberFromName`