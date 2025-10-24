# Method `Au.sqliteStatement.Reset`

Calls `sqlite3_reset` and/or `sqlite3_clear_bindings`.

```
public sqliteStatement Reset(bool resetStatement = true, bool clearBindings = true)
```

##### Parameters

- *resetStatement*  (`bool`):
    Call `sqlite3_reset`. Default `true`.
- *clearBindings*  (`bool`):
    Call `sqlite3_clear_bindings`. Default `true`.

##### Returns

`Au.sqliteStatement`

this.