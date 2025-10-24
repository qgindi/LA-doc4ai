# Method `Au.sqliteStatement.GetLong`

Calls `sqlite3_column_int64`.

```
public long GetLong(SLIndexOrName column)
```

##### Parameters

- *column*  (`Au.Types.SLIndexOrName`):
    Column name of 0-based index in results.

##### Returns

`long`

##### Exceptions

- `Au.Types.SLException`:
    The column does not exist in query results.

#### Remarks

Use this function to get integer values of size 8 bytes: `long`, `ulong`, 64-bit enum, maybe `System.DateTime`.