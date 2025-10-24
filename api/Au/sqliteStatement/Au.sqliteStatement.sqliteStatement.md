# Constructor of `Au.sqliteStatement`

Calls `sqlite3_prepare16_v3`.

```
public sqliteStatement(sqlite db, string sql, bool persistent = false)
```

##### Parameters

- *db*  (`Au.sqlite`)
- *sql*  (`string`):
    Single SQL statement.
- *persistent*  (`bool`):
    Use flag `SQLITE_PREPARE_PERSISTENT`.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.