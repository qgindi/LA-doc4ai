# Method `Au.csvTable.load`

Loads and parses a CSV file.

```
public static csvTable load(string file, char separator = ',', char quote = '"', bool trimSpaces = true)
```

##### Parameters

- *file*  (`string`):
    File. Must be full path. Can contain environment variables etc, see `Au.pathname.expand`.
- *separator*  (`char`):
    Field separator character used in CSV text. Default `','`.
- *quote*  (`char`):
    Character used in CSV text to enclose some fields. Default `'"'`.
- *trimSpaces*  (`bool`):
    Ignore ASCII space and tab characters surrounding fields in CSV text. Default `true`.

##### Returns

`Au.csvTable`

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Exception`:
    Exceptions of `System.IO.File.ReadAllText`.
- `FormatException`:
    Invalid CSV, eg contains incorrectly enclosed fields.

#### Remarks

Calls `System.IO.File.ReadAllText` and `Au.csvTable.parse`. Also uses `Au.filesystem.waitIfLocked`.