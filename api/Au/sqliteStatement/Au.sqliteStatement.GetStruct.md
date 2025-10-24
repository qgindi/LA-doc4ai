# Method `Au.sqliteStatement.GetStruct`

Calls `sqlite3_column_blob` and creates a variable of any value type that does not have fields of reference types.

```
public T GetStruct<T>(SLIndexOrName column) where T : unmanaged
```

##### Parameters

- *column*  (`Au.Types.SLIndexOrName`):
    Column name of 0-based index in results.

##### Returns

`T`

##### Exceptions

- `Au.Types.SLException`:
    The column does not exist in query results.

##### Type Parameters

- `T`