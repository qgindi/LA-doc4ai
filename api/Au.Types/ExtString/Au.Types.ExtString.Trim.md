# Method `Au.Types.ExtString.Trim`

Removes specified characters from the start and end of this string.

```
public static string Trim(this string t, string chars)
```

##### Parameters

- *t*  (`string`):
    This string.
- *chars*  (`string`):
    Characters to remove.

##### Returns

`string`

The result string.

##### Exceptions

- `ArgumentNullException`:
    *chars* is `null`.