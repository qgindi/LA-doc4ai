# Method `Au.Types.RXCalloutData.Group`

Gets the start index and length of the specified group in the subject string.

```
public (int index, int length) Group(int group)
```

##### Parameters

- *group*  (`int`):
    Group number (1-based index).

##### Returns

`(int start, int end)`

##### Exceptions

- `ArgumentOutOfRangeException`:
    *group* must be > 0 and \< `Au.Types.RXCalloutData.capture_top`.