# Class `Au.Types.SLTransaction`

A SQLite transaction or savepoint. The main purpose is to automatically rollback if not explicitly committed. Usage: `using(var trans = new SLTransaction(db)) { ... trans.Commit(); }`

```
public sealed class SLTransaction : IDisposable
```

##### Inheritance

`object` → `SLTransaction`

### Constructors

`SLTransaction(sqlite, string, string)`

### Properties

`SqlOfDispose`

### Methods

`Commit`, `Dispose`, `Rollback`