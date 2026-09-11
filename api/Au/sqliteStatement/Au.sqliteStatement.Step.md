# Method `Au.sqliteStatement.Step`

Calls `sqlite3_step`, and returns `true` if results data available (`sqlite3_step` returned `SQLITE_ROW`).

```csharp
public bool Step()
```

##### Returns

`bool`

##### Exceptions

- `Au.Types.SLException`:
  Failed.