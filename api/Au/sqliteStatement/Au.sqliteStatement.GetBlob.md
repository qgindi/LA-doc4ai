# Method `Au.sqliteStatement.GetBlob`

## Overload 1

Calls `sqlite3_column_blob`.

```
public byte* GetBlob(SLIndexOrName column, out int nBytes)
```

##### Parameters

- *column*  (`Au.Types.SLIndexOrName`):
    Column name of 0-based index in results.
- *nBytes*  (`int`):
    Blob size.

##### Returns

`byte*`

The returned memory is managed by SQLite and will become invalid when calling other SQLite functions afterwards. For zero-length BLOB returns `null`.

##### Exceptions

- `Au.Types.SLException`:
    The column does not exist in query results.

* * *

## Overload 2

Calls `sqlite3_column_blob`.

```
public ReadOnlySpan<byte> GetBlob(SLIndexOrName column)
```

##### Parameters

- *column*  (`Au.Types.SLIndexOrName`):
    Column name of 0-based index in results.

##### Returns

`ReadOnlySpan<byte>`

The returned memory is managed by SQLite and will become invalid when calling other SQLite functions afterwards.

##### Exceptions

- `Au.Types.SLException`:
    The column does not exist in query results.

* * *

## Overload 3

Calls `sqlite3_column_blob`.

```
public ReadOnlySpan<T> GetBlob<T>(SLIndexOrName column) where T : unmanaged
```

##### Parameters

- *column*  (`Au.Types.SLIndexOrName`):
    Column name of 0-based index in results.

##### Returns

`ReadOnlySpan<T>`

The returned memory is managed by SQLite and will become invalid when calling other SQLite functions afterwards.

##### Exceptions

- `Au.Types.SLException`:
    The column does not exist in query results.

##### Type Parameters

- `T`