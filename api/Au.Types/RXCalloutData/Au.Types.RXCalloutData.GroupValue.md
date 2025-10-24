# Method `Au.Types.RXCalloutData.GroupValue`

Gets the value (substring) of the specified group.

```
public string GroupValue(int group)
```

##### Parameters

- *group*  (`int`):
    Group number (1-based index).

##### Returns

`string`

##### Exceptions

- `ArgumentOutOfRangeException`:
    *group* must be > 0 and \< `Au.Types.RXCalloutData.capture_top`.