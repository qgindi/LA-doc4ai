# Method `Au.sqlite.Execute`

## Overload 1

Calls `sqlite3_exec` to execute one or more SQL statements that don't return data.

```
public void Execute(string sql)
```

##### Parameters

- *sql*  (`string`):
    SQL statement, or several `;`-separated statements.

##### Exceptions

- `Au.Types.SLException`:
    Failed to execute *sql*.

* * *

## Overload 2

Executes single SQL statement that does not return data. Binds values.

```
public void Execute(string sql, params object[] bind)
```

##### Parameters

- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

* * *

## Overload 3

Executes single SQL statement that does not return data. To bind values calls callback function.

```
public void Execute(string sql, Action<sqliteStatement> bind)
```

##### Parameters

- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`Action<Au.sqliteStatement>`):
    Callback function that should bind (`Au.sqliteStatement.Bind`) values to `?` characters in *sql*. Read about SQL parameters in SQLite website.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.