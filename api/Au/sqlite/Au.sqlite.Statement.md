# Method `Au.sqlite.Statement`

## Overload 1

Returns `new sqliteStatement(this, sql)`.

```
public sqliteStatement Statement(string sql)
```

##### Parameters

- *sql*  (`string`):
    Single SQL statement. This function does not execute it.

##### Returns

`Au.sqliteStatement`

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

### See Also

`Au.sqliteStatement`

* * *

## Overload 2

Returns `new sqliteStatement(this, sql).BindAll(bind)`.

```
public sqliteStatement Statement(string sql, params object[] bind)
```

##### Parameters

- *sql*  (`string`):
    Single SQL statement. This function does not execute it.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Optional. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Returns

`Au.sqliteStatement`

##### Exceptions

- `NotSupportedException`:

    - *sql* contains more than single SQL statement.
    - A *bind* value is of an unsupported type.
- `Au.Types.SLException`:
    Failed.

### See Also

`Au.sqliteStatement`

`Au.sqliteStatement.BindAll`