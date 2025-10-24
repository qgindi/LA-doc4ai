# Method `Au.keys.more.parseKeysString`

Converts keys string to `Au.Types.KKey` array.

```
public static KKey[] parseKeysString(string keys_)
```

##### Parameters

- *keys_*  (`string`):
    String containing one or more [key names](../articles/Key%20names%20and%20operators.html). Operators are not supported.

##### Returns

`Au.Types.KKey[]`

##### Exceptions

- `ArgumentException`:
    Error in *keys_* string.