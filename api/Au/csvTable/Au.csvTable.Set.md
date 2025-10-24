# Method `Au.csvTable.Set`

## Overload 1

Converts a number to string and sets a field.

```
public void Set(Index row, int column, int value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index. Can be from the end; for example `^1` is the last row. Adds new row if `^0`.
- *column*  (`int`):
    0-based column index. If >= `Au.csvTable.ColumnCount` and \< 1000, sets `ColumnCount = column + 1`.
- *value*  (`int`)

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 2

Converts a number to hex string and sets a field.

```
public void Set(Index row, int column, uint value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index. Can be from the end; for example `^1` is the last row. Adds new row if `^0`.
- *column*  (`int`):
    0-based column index. If >= `Au.csvTable.ColumnCount` and \< 1000, sets `ColumnCount = column + 1`.
- *value*  (`uint`)

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 3

Converts a number to string and sets a field.

```
public void Set(Index row, int column, long value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index. Can be from the end; for example `^1` is the last row. Adds new row if `^0`.
- *column*  (`int`):
    0-based column index. If >= `Au.csvTable.ColumnCount` and \< 1000, sets `ColumnCount = column + 1`.
- *value*  (`long`)

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 4

Converts a number to hex string and sets a field.

```
public void Set(Index row, int column, ulong value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index. Can be from the end; for example `^1` is the last row. Adds new row if `^0`.
- *column*  (`int`):
    0-based column index. If >= `Au.csvTable.ColumnCount` and \< 1000, sets `ColumnCount = column + 1`.
- *value*  (`ulong`)

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 5

Converts a number to string and sets a field.

```
public void Set(Index row, int column, double value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index. Can be from the end; for example `^1` is the last row. Adds new row if `^0`.
- *column*  (`int`):
    0-based column index. If >= `Au.csvTable.ColumnCount` and \< 1000, sets `ColumnCount = column + 1`.
- *value*  (`double`)

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 6

Converts a number to string and sets a field.

```
public void Set(Index row, int column, float value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index. Can be from the end; for example `^1` is the last row. Adds new row if `^0`.
- *column*  (`int`):
    0-based column index. If >= `Au.csvTable.ColumnCount` and \< 1000, sets `ColumnCount = column + 1`.
- *value*  (`float`)

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 7

Converts a `bool` to string `"true"` or `"false"` and sets a field.

```
public void Set(Index row, int column, bool value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index. Can be from the end; for example `^1` is the last row. Adds new row if `^0`.
- *column*  (`int`):
    0-based column index. If >= `Au.csvTable.ColumnCount` and \< 1000, sets `ColumnCount = column + 1`.
- *value*  (`bool`)

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.