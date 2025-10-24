# Method `Au.sqliteStatement.GetDouble`

Calls `sqlite3_column_double`.

```
public double GetDouble(SLIndexOrName column)
```

##### Parameters

- *column*  (`Au.Types.SLIndexOrName`):
    Column name of 0-based index in results.

##### Returns

`double`

##### Exceptions

- `Au.Types.SLException`:
    The column does not exist in query results.