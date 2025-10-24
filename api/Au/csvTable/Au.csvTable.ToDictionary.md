# Method `Au.csvTable.ToDictionary`

## Overload 1

Creates dictionary from this 2-column CSV table.

```
public Dictionary<string, string> ToDictionary(bool ignoreCase, bool ignoreDuplicates)
```

##### Parameters

- *ignoreCase*  (`bool`):
    Case-insensitive dictionary keys.
- *ignoreDuplicates*  (`bool`):
    Don't throw exception if column 0 contains duplicate strings. Replace old value with new value.

##### Returns

`Dictionary<string, string>`

##### Exceptions

- `InvalidOperationException`:
    `Au.csvTable.ColumnCount` not 2.
- `ArgumentException`:
    Column 0 contains duplicate strings.

* * *

## Overload 2

Creates dictionary from this CSV table of any column count, using a callback function to convert cell strings to dictionary values of any type.

```
public Dictionary<string, T> ToDictionary<T>(bool ignoreCase, bool ignoreDuplicates, Func<string[], T> rowToValue)
```

##### Parameters

- *ignoreCase*  (`bool`):
    Case-insensitive dictionary keys.
- *ignoreDuplicates*  (`bool`):
    Don't throw exception if column 0 contains duplicate strings. Replace old value with new value.
- *rowToValue*  (`Func<string[], T>`):
    Callback function that converts one or more cell strings to single value of type `T`. The array is whole row; element 0 is key, and usually is not used.

##### Returns

`Dictionary<string, T>`

##### Exceptions

- `ArgumentNullException`
- `InvalidOperationException`:
    `Au.csvTable.ColumnCount` less than 2.
- `ArgumentException`:
    Column 0 contains duplicate strings.

##### Type Parameters

- `T`