# Method `Au.Types.SLTransaction.Dispose`

Calls `Au.Types.SLTransaction.Rollback` if not called `Au.Types.SLTransaction.Commit` or `Au.Types.SLTransaction.Rollback`.

```csharp
public void Dispose()
```

##### Exceptions

- `Au.Types.SLException`:
  Failed to execute `Au.Types.SLTransaction.SqlOfDispose`.

##### Implements

`IDisposable.Dispose()`