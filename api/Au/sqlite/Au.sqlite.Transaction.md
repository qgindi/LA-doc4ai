# Method `Au.sqlite.Transaction`

Returns `new SLTransaction(this, sql, sqlOfDispose)`. See `Au.Types.SLTransaction.SLTransaction`.

```
public SLTransaction Transaction(string sql = "BEGIN", string sqlOfDispose = "ROLLBACK")
```

##### Parameters

- *sql*  (`string`):
    SQL to execute now. Default `"BEGIN"`. For nested transaction use `"SAVEPOINT name"`.
- *sqlOfDispose*  (`string`):
    SQL to execute when disposing the `Au.Types.SLTransaction` variable if not called `Au.Types.SLTransaction.Commit` or `Au.Types.SLTransaction.Rollback`. Default `"ROLLBACK"`. For nested transaction use `"ROLLBACK TO name"`. See also: `Au.Types.SLTransaction.SqlOfDispose`.

##### Returns

`Au.Types.SLTransaction`

##### Exceptions

- `Au.Types.SLException`:
    Failed to execute *sql*.