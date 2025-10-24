# Constructor of `Au.sqlite`

Opens or creates a database file.

```
public sqlite(string file, SLFlags flags = SLFlags.ReadWriteCreate, string sql = null)
```

##### Parameters

- *file*  (`string`):

    Database file. Can be:

    - Full path. Supports environment variables etc, see `Au.pathname.expand`
    - `":memory:"` - create a private, temporary in-memory database.
    - `""` - create a private, temporary on-disk database.
    - Starts with `"file:"` - see `sqlite3_open_v2`.
- *flags*  (`Au.Types.SLFlags`):
    `sqlite3_open_v2` flags. Default: read-write, create file if does not exist (and parent directory).
- *sql*  (`string`):
    SQL to execute. For example, one or more ;-separated `PRAGMA` statements to configure the database connection. Or even `"CREATE TABLE IF NOT EXISTS ..."`. This function also always executes `"PRAGMA foreign_keys=ON;PRAGMA secure_delete=ON;"`.

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Au.Types.SLException`:
    Failed to open database or execute *sql*.

#### Remarks

Calls `sqlite3_open_v2`.

> **Note:**
> If a variable of this class is used by multiple threads, use `lock(variable) { }` where need.