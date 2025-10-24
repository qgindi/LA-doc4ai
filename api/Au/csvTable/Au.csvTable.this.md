# Indexer of `Au.csvTable`

## Overload 1

Gets or sets a field.

```
public string this[int row, int column] { get; set; }
```

##### Parameters

- *row*  (`int`):
    0-based row index. The `set` function adds new row if negative or equal to `Au.csvTable.RowCount`.
- *column*  (`int`):
    0-based column index. With the `set` function it can be >= `Au.csvTable.ColumnCount` and \< 1000; then sets `ColumnCount = column + 1`.

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`string`

#### Examples

```
var c = new csvTable { ColumnCount = 2 };
c[0, 0] = "A1";
c[0, 1] = "A2";
c[1, 0] = "B1";
c[1, 1] = "B2";
print.it(c);
string s = c[0, 0];
print.it(s);
```

* * *

## Overload 2

Gets or sets a field.

```
public string this[Index row, int column] { get; set; }
```

##### Parameters

- *row*  (`Index`):
    0-based row index. Can be from the end; for example `^1` is the last row. The `set` function adds new row if `^0`.
- *column*  (`int`):
    0-based column index. With the `set` function it can be >= `Au.csvTable.ColumnCount` and \< 1000; then sets `ColumnCount = column + 1`.

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`string`

* * *

## Overload 3

Gets or sets fields in a row.

```
public string[] this[int row] { get; set; }
```

##### Parameters

- *row*  (`int`):
    0-based row index. The `set` function adds new row if negative or equal to `Au.csvTable.RowCount`.

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`string[]`

#### Remarks

The `get` function gets the row array. It's not a copy; changing its elements will change content of this `Au.csvTable` variable. The `set` function sets the row array. Does not copy the array, unless its `Length` is less than `Au.csvTable.ColumnCount`.

#### Examples

```
var c = new csvTable();
c[-1] = ["A", "B"];
c[-1] = ["C", "D"];
print.it(c);
for (int row = 0; row < c.RowCount; row++) {
	print.it(c[row, 0], c[row, 1]);
}
```

* * *

## Overload 4

Gets or sets fields in a row.

```
public string[] this[Index row] { get; set; }
```

##### Parameters

- *row*  (`Index`):
    0-based row index. Can be from the end; for example `^1` is the last row. The `set` function adds new row if `^0`.

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`string[]`

#### Remarks

The `get` function gets the row array. It's not a copy; changing its elements will change content of this `Au.csvTable` variable. The `set` function sets the row array. Does not copy the array, unless its `Length` is less than `Au.csvTable.ColumnCount`.