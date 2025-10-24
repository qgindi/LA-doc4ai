# Method `Au.sqlite.GetStruct`

Executes single SQL statement and gets single value.

```
public bool GetStruct<T>(out T value, string sql, params object[] bind) where T : unmanaged
```

##### Parameters

- *value*  (`T`):
    Receives data.
- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Returns

`bool`

`false` if the statement returned no data.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

##### Type Parameters

- `T`

#### Remarks

Can be used to get various value types, for example `decimal`, `System.Guid`, `Au.Types.RECT`.