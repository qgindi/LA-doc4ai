# Method `Au.sqliteStatement.GetList`

Calls `sqlite3_column_blob` and creates `List<T>`.

```
public List<T> GetList<T>(SLIndexOrName column) where T : unmanaged
```

##### Parameters

- *column*  (`Au.Types.SLIndexOrName`):
    Column name of 0-based index in results.

##### Returns

`List<T>`

##### Exceptions

- `Au.Types.SLException`:
    The column does not exist in query results.

##### Type Parameters

- `T`