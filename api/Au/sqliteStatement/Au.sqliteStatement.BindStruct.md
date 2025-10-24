# Method `Au.sqliteStatement.BindStruct`

Binds a value as blob. Calls `sqlite3_bind_blob64`.

```
public sqliteStatement BindStruct<T>(SLIndexOrName sqlParam, T value) where T : unmanaged
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *value*  (`T`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

##### Type Parameters

- `T`

#### Remarks

Can be any value type that does not contain fields of reference types. Examples: `System.Guid`, `Au.Types.POINT`, `int`, `decimal`.