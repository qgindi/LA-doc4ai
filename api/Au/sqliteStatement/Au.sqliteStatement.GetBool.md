# Method `Au.sqliteStatement.GetBool`

Calls `sqlite3_column_int64` and returns `true` if the value is not 0.

```
public bool GetBool(SLIndexOrName column)
```

##### Parameters

- *column*  (`Au.Types.SLIndexOrName`):
    Column name of 0-based index in results.

##### Returns

`bool`

##### Exceptions

- `Au.Types.SLException`:
    The column does not exist in query results.