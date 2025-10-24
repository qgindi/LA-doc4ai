# Method `Au.keys.more.parseKeyName`

## Overload 1

Converts key name to `Au.Types.KKey`.

```
public static KKey parseKeyName(string keyName)
```

##### Parameters

- *keyName*  (`string`):
    [Key name](../articles/Key%20names%20and%20operators.html).

##### Returns

`Au.Types.KKey`

0 if unknown key name.

* * *

## Overload 2

Converts key name to `Au.Types.KKey`.

```
public static KKey parseKeyName(string s, int startIndex, int length)
```

##### Parameters

- *s*  (`string`):
    String containing [key name](../articles/Key%20names%20and%20operators.html).
- *startIndex*  (`int`):
    Key name start index in *s*.
- *length*  (`int`):
    Key name length.

##### Returns

`Au.Types.KKey`

0 if unknown key name.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *startIndex* or *length*.