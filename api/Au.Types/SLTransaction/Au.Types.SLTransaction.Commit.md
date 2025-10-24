# Method `Au.Types.SLTransaction.Commit`

Executes a commit SQL and disables `Au.Types.SLTransaction.Dispose`.

```
public void Commit(string sql = "COMMIT")
```

##### Parameters

- *sql*  (`string`):
    SQL to execute. Default `"COMMIT"`. For nested transaction use `"RELEASE name"`.

##### Exceptions

- `Au.Types.SLException`:
    Failed to execute *sql*.