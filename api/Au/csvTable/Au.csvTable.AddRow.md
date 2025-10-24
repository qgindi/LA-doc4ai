# Method `Au.csvTable.AddRow`

Adds new row and sets its fields.

```
public void AddRow(params string[] fields)
```

##### Parameters

- *fields*  (`string[]`):
    Row fields. Can be a string array or multiple string arguments. Does not copy the array, unless its `Length` is less than `Au.csvTable.ColumnCount`. Adds new columns if array `Length` (or the number of string arguments) is greater than `ColumnCount`.

##### Exceptions

- `ArgumentOutOfRangeException`