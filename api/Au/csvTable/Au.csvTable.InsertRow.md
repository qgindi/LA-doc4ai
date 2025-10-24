# Method `Au.csvTable.InsertRow`

## Overload 1

Inserts new row and sets its fields.

```
public void InsertRow(int index, params string[] fields)
```

##### Parameters

- *index*  (`int`):
    0-based row index. If negative or equal to `Au.csvTable.RowCount`, adds to the end.
- *fields*  (`string[]`):
    Row fields. Can be a string array or multiple string arguments. Does not copy the array, unless its `Length` is less than `Au.csvTable.ColumnCount`. Adds new columns if array `Length` (or the number of string arguments) is greater than `ColumnCount`.

##### Exceptions

- `ArgumentOutOfRangeException`

* * *

## Overload 2

Inserts new empty row.

```
public void InsertRow(int index)
```

##### Parameters

- *index*  (`int`):
    0-based row index. If negative or equal to `Au.csvTable.RowCount`, adds to the end.

##### Exceptions

- `ArgumentOutOfRangeException`