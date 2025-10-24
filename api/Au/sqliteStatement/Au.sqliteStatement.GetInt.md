# Method `Au.sqliteStatement.GetInt`

Calls `sqlite3_column_int`.

```
public int GetInt(SLIndexOrName column)
```

##### Parameters

- *column*  (`Au.Types.SLIndexOrName`):
    Column name of 0-based index in results.

##### Returns

`int`

##### Exceptions

- `Au.Types.SLException`:
    The column does not exist in query results.

#### Remarks

Use this function to get integer values of size 4, 2 or 1 bytes: `int`, `uint`, `short`, `ushort`, `byte`, `sbyte`, enum.