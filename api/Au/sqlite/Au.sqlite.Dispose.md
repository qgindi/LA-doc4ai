# Method `Au.sqlite.Dispose`

## Overload 1

```csharp
protected virtual void Dispose(bool disposing)
```

##### Parameters

- *disposing*  (`bool`)

* * *

## Overload 2

Calls `sqlite3_close_v2`.
If fails, prints a warning.

```csharp
public void Dispose()
```

##### Implements

`IDisposable.Dispose()`