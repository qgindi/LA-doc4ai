# Method `Au.sqliteStatement.GetText`

Calls `sqlite3_column_text`.

```
public string GetText(SLIndexOrName column)
```

##### Parameters

- *column*  (`Au.Types.SLIndexOrName`):
    Column name of 0-based index in results.

##### Returns

`string`

##### Exceptions

- `Au.Types.SLException`:
    The column does not exist in query results.