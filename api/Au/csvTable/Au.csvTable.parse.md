# Method `Au.csvTable.parse`

Parses CSV string and creates new `Au.csvTable` variable that contains data in internal `List` of string arrays.

```
public static csvTable parse(string csv, char separator = ',', char quote = '"', bool trimSpaces = true)
```

##### Parameters

- *csv*  (`string`):
    CSV text. If rows in CSV text have different field count, the longest row sets the `Au.csvTable.ColumnCount` property and lengths of all row arrays; array elements of missing CSV fields will be `null`.
- *separator*  (`char`):
    Field separator character used in CSV text. Default `','`.
- *quote*  (`char`):
    Character used in CSV text to enclose some fields. Default `'"'`.
- *trimSpaces*  (`bool`):
    Ignore ASCII space and tab characters surrounding fields in CSV text. Default `true`.

##### Returns

`Au.csvTable`

##### Exceptions

- `FormatException`:
    Invalid CSV, eg contains incorrectly enclosed fields.