# Method `Au.sqlite.Get`

## Overload 1

Executes single SQL statement and gets single value.

```
public bool Get(out int value, string sql, params object[] bind)
```

##### Parameters

- *value*  (`int`):
    Receives data.
- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Returns

`bool`

`false` if the statement returned no data.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

#### Remarks

Also can be used to get `uint`, `short`, `ushort`, `byte`, `sbyte`, enum. Will need to cast from `int`.

* * *

## Overload 2

Executes single SQL statement and gets single value.

```
public bool Get(out long value, string sql, params object[] bind)
```

##### Parameters

- *value*  (`long`):
    Receives data.
- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Returns

`bool`

`false` if the statement returned no data.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

#### Remarks

Also can be used to get `ulong`, 64-bit enum, maybe `System.DateTime`.

* * *

## Overload 3

Executes single SQL statement and gets single value.

```
public bool Get(out bool value, string sql, params object[] bind)
```

##### Parameters

- *value*  (`bool`):
    Receives data.
- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Returns

`bool`

`false` if the statement returned no data.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

* * *

## Overload 4

Executes single SQL statement and gets single value.

```
public bool Get(out double value, string sql, params object[] bind)
```

##### Parameters

- *value*  (`double`):
    Receives data.
- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Returns

`bool`

`false` if the statement returned no data.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

#### Remarks

Also can be used to get `float`.

* * *

## Overload 5

Executes single SQL statement and gets single value.

```
public bool Get(out string value, string sql, params object[] bind)
```

##### Parameters

- *value*  (`string`):
    Receives data.
- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Returns

`bool`

`false` if the statement returned no data.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

* * *

## Overload 6

Executes single SQL statement and gets single value.

```
public bool Get<T>(out T[] value, string sql, params object[] bind) where T : unmanaged
```

##### Parameters

- *value*  (`T[]`):
    Receives data.
- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Returns

`bool`

`false` if the statement returned no data.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

##### Type Parameters

- `T`

* * *

## Overload 7

Executes single SQL statement and gets single value.

```
public bool Get<T>(out List<T> value, string sql, params object[] bind) where T : unmanaged
```

##### Parameters

- *value*  (`List<T>`):
    Receives data.
- *sql*  (`string`):
    Single SQL statement.
- *bind*  (`object[]`):
    Values that will replace `?` characters in *sql*. Read about SQL parameters in SQLite website. Supported types: `Au.sqliteStatement.BindAll`. Example: `Au.sqlite`.

##### Returns

`bool`

`false` if the statement returned no data.

##### Exceptions

- `Au.Types.SLException`:
    Failed.
- `NotSupportedException`:
    *sql* contains more than single SQL statement.

##### Type Parameters

- `T`