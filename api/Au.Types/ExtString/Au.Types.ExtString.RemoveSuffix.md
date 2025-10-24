# Method `Au.Types.ExtString.RemoveSuffix`

## Overload 1

Removes *suffix* string from the end.

```
public static string RemoveSuffix(this string t, string suffix, bool ignoreCase = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *suffix*  (`string`):
    Substring to remove.
- *ignoreCase*  (`bool`):
    Case-insensitive.

##### Returns

`string`

The result string. Returns this string if does not end with *suffix*.

##### Exceptions

- `ArgumentNullException`:
    *suffix* is `null`.

* * *

## Overload 2

Removes *suffix* character from the end.

```
public static string RemoveSuffix(this string t, char suffix)
```

##### Parameters

- *t*  (`string`):
    This string.
- *suffix*  (`char`):
    Character to remove.

##### Returns

`string`

The result string. Returns this string if does not end with *suffix*.

##### Exceptions

- `ArgumentNullException`:
    *suffix* is `null`.