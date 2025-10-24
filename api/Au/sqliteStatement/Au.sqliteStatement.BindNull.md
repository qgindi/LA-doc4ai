# Method `Au.sqliteStatement.BindNull`

Calls `sqlite3_bind_null`.

```
public sqliteStatement BindNull(SLIndexOrName sqlParam)
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

#### Remarks

Usually don't need to call this function. Unset parameter values are null. The `Bind` functions set null too if the value is null.