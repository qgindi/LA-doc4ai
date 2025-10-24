# Method `Au.sqliteStatement.BindAll`

Binds multiple values of any supported types.

```
public sqliteStatement BindAll(params object[] values)
```

##### Parameters

- *values*  (`object[]`):

    Values that will replace `?` characters in SQL. Read about SQL parameters in SQLite website. Example: `Au.sqlite`. Supported types:

    - `int`, `uint`, `byte`, `sbyte`, `short`, `ushort` - calls `sqlite3_bind_int`.
    - `bool` - calls `sqlite3_bind_int` (0 or 1).
    - `long`, `ulong` - calls `sqlite3_bind_int64`.
    - `double`, `float` - calls `sqlite3_bind_double`.
    - `string` - calls `sqlite3_bind_text16`.
    - `decimal` - calls `sqlite3_bind_blob64`.
    - `Guid` - calls `sqlite3_bind_blob64`.
    - `Array` - calls `sqlite3_bind_blob64`.
    - An `enum` type - calls `sqlite3_bind_int` or `sqlite3_bind_int64`.

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `NotSupportedException`:
    A value is of an unsupported type.
- `Au.Types.SLException`:
    Failed.

#### Remarks

For each parameter calls a `sqlite3_bind_x` function depending on type. Uses index 1, 2 and so on. This function is an alternative to calling `BindX` functions for each parameter. However it supports less types and adds boxing overhead. Does not call `sqlite3_reset` and `sqlite3_clear_bindings`. If need, call `Au.sqliteStatement.Reset` before.