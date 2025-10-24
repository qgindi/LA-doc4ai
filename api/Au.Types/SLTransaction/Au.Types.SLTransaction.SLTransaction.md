# Constructor of `Au.Types.SLTransaction`

Begins a SQLite transaction and prepares for automatic rollback if not explicitly committed. Usage: `using(var trans = new SLTransaction(db)) { ... trans.Commit(); }`

```
public SLTransaction(sqlite db, string sql = "BEGIN", string sqlOfDispose = "ROLLBACK")
```

##### Parameters

- *db*  (`Au.sqlite`)
- *sql*  (`string`):
    SQL to execute now. Default `"BEGIN"`. For nested transaction use `"SAVEPOINT name"`.
- *sqlOfDispose*  (`string`):
    SQL to execute when disposing the `Au.Types.SLTransaction` variable if not called `Au.Types.SLTransaction.Commit` or `Au.Types.SLTransaction.Rollback`. Default `"ROLLBACK"`. For nested transaction use `"ROLLBACK TO name"`. See also: `Au.Types.SLTransaction.SqlOfDispose`.

##### Exceptions

- `Au.Types.SLException`:
    Failed to execute *sql*.