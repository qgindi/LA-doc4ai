# Method `Au.sqlite.Any`

Executes single SQL statement and returns `true` if it returns at least one row of data.

```
public bool Any(string sql, params object[] bind)
```

##### Parameters

- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Returns

`bool`

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

#### Remarks

This function is similar to the `GetX` functions, but it does not retrieve the data.