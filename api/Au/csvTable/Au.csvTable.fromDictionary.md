# Method `Au.csvTable.fromDictionary`

## Overload 1

Creates 2-column CSV table from dictionary keys and values of type `string`.

```
public static csvTable fromDictionary(Dictionary<string, string> d)
```

##### Parameters

- *d*  (`Dictionary<string, string>`)

##### Returns

`Au.csvTable`

##### Exceptions

- `ArgumentNullException`

* * *

## Overload 2

Creates 2-column CSV table from dictionary keys and values of any type, using a callback function to convert values to `string`.

```
public static csvTable fromDictionary<T>(Dictionary<string, T> d, Func<T, string> valueToString)
```

##### Parameters

- *d*  (`Dictionary<string, T>`)
- *valueToString*  (`Func<T, string>`):
    Callback function that converts value of type `T` to `string`.

##### Returns

`Au.csvTable`

##### Exceptions

- `ArgumentNullException`

##### Type Parameters

- `T`

* * *

## Overload 3

Creates CSV table of any column count from dictionary keys and values of any type, using a callback function to convert values to cell strings.

```
public static csvTable fromDictionary<T>(Dictionary<string, T> d, int columnCount, Action<T, string[]> valueToCells)
```

##### Parameters

- *d*  (`Dictionary<string, T>`)
- *columnCount*  (`int`):
    CSV column count. Must be 2 or more.
- *valueToCells*  (`Action<T, string[]>`):
    Callback function that converts value of type `T` to one or more strings and puts them in row array elements starting from index 1. At index 0 is key.

##### Returns

`Au.csvTable`

##### Exceptions

- `ArgumentNullException`
- `ArgumentOutOfRangeException`:
    *columnCount* less than 2.

##### Type Parameters

- `T`