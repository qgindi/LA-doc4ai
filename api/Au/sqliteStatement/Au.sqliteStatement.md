# Class `Au.sqliteStatement`

Creates and executes a SQLite prepared statement.

```
public class sqliteStatement : IDisposable
```

##### Remarks

This class wraps a SQLite API object `sqlite3_stmt*` and related `sqlite3_x` functions. They are documented perfectly in the SQLite website. More info and example: `Au.sqlite`.

> **Important:**
> A variable of this class can be used by multiple threads, but not simultaneously. Use `lock(database) { }` where need.

##### Inheritance

`object` → `sqliteStatement`

### Constructors

`sqliteStatement(sqlite, string, bool)`

### Properties

`ColumnCount`, `DB`, `Handle`

### Methods

`Bind`, `Bind`, `Bind`, `Bind`, `Bind`, `Bind`, `Bind`, `Bind`, `BindAll`, `BindNull`, `BindStruct<T>`, `Bind<T>`, `Bind<T>`, `Bind<T>`, `Bind<T>`, `Bind<T>`, `ColumnIndex`, `ColumnName`, `Dispose`, `Dispose`, `GetArray<T>`, `GetBlob`, `GetBlob`, `GetBlob<T>`, `GetBool`, `GetDouble`, `GetInt`, `GetList<T>`, `GetLong`, `GetStruct<T>`, `GetText`, `Reset`, `Step`

### Operators

`implicit operator nint(sqliteStatement)`