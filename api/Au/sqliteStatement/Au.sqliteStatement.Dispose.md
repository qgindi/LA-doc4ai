# Method `Au.sqliteStatement.Dispose`

## Overload 1

```
protected virtual void Dispose(bool disposing)
```

##### Parameters

- *disposing*  (`bool`)

* * *

## Overload 2

Calls `sqlite3_finalize`.

```
public void Dispose()
```

##### Implements

`IDisposable.Dispose()`