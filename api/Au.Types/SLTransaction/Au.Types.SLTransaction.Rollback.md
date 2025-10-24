# Method `Au.Types.SLTransaction.Rollback`

Executes a rollback SQL (if in transaction) and disables `Au.Types.SLTransaction.Dispose`. Usually don't need to call this function explicitly. It is implicitly called when disposing this variable if the transaction was not committed.

```
public void Rollback(string sql = null)
```

##### Parameters

- *sql*  (`string`):
    SQL to execute. Default: `Au.Types.SLTransaction.SqlOfDispose`.

##### Exceptions

- `Au.Types.SLException`:
    Failed to execute *sql*.