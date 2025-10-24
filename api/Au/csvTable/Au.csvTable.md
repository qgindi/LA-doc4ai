# Class `Au.csvTable`

Parses and composes CSV text. CSV table data in memory as a `List` of string arrays.

```
public class csvTable
```

##### Remarks

CSV is a text format used to store a single table of data in human-readable/editable way. It is a list of lines (called rows or records) containing one or more values (called fields or cells) separated by a separator character.

There is no strictly defined CSV standard. This class uses these rules:

- Fields containing separator characters (default `','`), quote characters (default `'"'`) and multiple lines are enclosed in quote characters. Example: `"ab, cd"`.
- Each quote character in such fields is escaped (replaced) with two quote characters. Example: `"ab ""cd"" ef"`.
- If a field value starts or ends with ASCII space or tab characters, it is enclosed in quote characters. Example: `" ab "`. Or use parameter *trimSpaces* `false` when parsing.
- Rows in CSV text can have different field count. All rows in in-memory CSV table have equal field count.

##### Examples

```
var c = new csvTable();
c.AddRow("A", "B");
c.AddRow("C", "D");
var csv = c.ToString();
print.it(csv);

var k = csvTable.parse(csv);
for (int row = 0; row < k.RowCount; row++) {
	print.it(k[row, 0], k[row, 1]);
}
```

##### Inheritance

`object` → `csvTable`

### Constructors

`csvTable()`

### Properties

`ColumnCount`, `this[Index]`, `this[Index, int]`, `this[int]`, `this[int, int]`, `Quote`, `RowCount`, `Rows`, `Separator`

### Methods

`AddRow`, `Get`, `Get`, `Get`, `Get`, `Get`, `Get`, `Get`, `InsertRow`, `InsertRow`, `RemoveRow`, `Save`, `Set`, `Set`, `Set`, `Set`, `Set`, `Set`, `Set`, `ToDictionary`, `ToDictionary<T>`, `ToString`, `fromDictionary`, `fromDictionary<T>`, `fromDictionary<T>`, `load`, `parse`