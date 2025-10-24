# Method `Au.sqliteStatement.Bind`

## Overload 1

Calls `sqlite3_bind_int`.

```
public sqliteStatement Bind(SLIndexOrName sqlParam, int value)
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *value*  (`int`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

* * *

## Overload 2

Calls `sqlite3_bind_int`.

```
public sqliteStatement Bind(SLIndexOrName sqlParam, uint value)
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *value*  (`uint`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

* * *

## Overload 3

Calls `sqlite3_bind_int64`.

```
public sqliteStatement Bind(SLIndexOrName sqlParam, long value)
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *value*  (`long`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

* * *

## Overload 4

Calls `sqlite3_bind_int64`.

```
public sqliteStatement Bind(SLIndexOrName sqlParam, ulong value)
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *value*  (`ulong`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

* * *

## Overload 5

Calls `sqlite3_bind_int` (0 or 1).

```
public sqliteStatement Bind(SLIndexOrName sqlParam, bool value)
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *value*  (`bool`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

* * *

## Overload 6

Binds an enum value as `int` or `long`. Calls `sqlite3_bind_int` or `sqlite3_bind_int64`.

```
public sqliteStatement Bind<T>(SLIndexOrName sqlParam, T value) where T : unmanaged, Enum
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *value*  (`T`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

##### Type Parameters

- `T`

* * *

## Overload 7

Calls `sqlite3_bind_double`.

```
public sqliteStatement Bind(SLIndexOrName sqlParam, double value)
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *value*  (`double`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

* * *

## Overload 8

Calls `sqlite3_bind_text16`.

```
public sqliteStatement Bind(SLIndexOrName sqlParam, string value)
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *value*  (`string`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

* * *

## Overload 9

Calls `sqlite3_bind_blob64`.

```
public sqliteStatement Bind(SLIndexOrName sqlParam, void* blob, long nBytes)
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *blob*  (`void*`)
- *nBytes*  (`long`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

* * *

## Overload 10

Calls `sqlite3_bind_blob64`.

```
public sqliteStatement Bind<T>(SLIndexOrName sqlParam, ReadOnlySpan<T> blob) where T : unmanaged
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *blob*  (`ReadOnlySpan<T>`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

##### Type Parameters

- `T`

* * *

## Overload 11

Calls `sqlite3_bind_blob64`.

```
public sqliteStatement Bind<T>(SLIndexOrName sqlParam, Span<T> blob) where T : unmanaged
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *blob*  (`Span<T>`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

##### Type Parameters

- `T`

* * *

## Overload 12

Calls `sqlite3_bind_blob64`.

```
public sqliteStatement Bind<T>(SLIndexOrName sqlParam, T[] array) where T : unmanaged
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *array*  (`T[]`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

##### Type Parameters

- `T`

* * *

## Overload 13

Calls `sqlite3_bind_blob64`.

```
public sqliteStatement Bind<T>(SLIndexOrName sqlParam, List<T> list) where T : unmanaged
```

##### Parameters

- *sqlParam*  (`Au.Types.SLIndexOrName`):
    Parameter name or 1-based index.
- *list*  (`List<T>`)

##### Returns

`Au.sqliteStatement`

this.

##### Exceptions

- `Au.Types.SLException`:
    Failed.

##### Type Parameters

- `T`