# Method `Au.sqliteStatement.ColumnIndex`

Finds column by name in results.

```
public int ColumnIndex(string name)
```

##### Parameters

- *name*  (`string`):
    Column name in results, as returned by `sqlite3_column_name`. Case-sensitive.

##### Returns

`int`

0-based index, or -1 if not found.