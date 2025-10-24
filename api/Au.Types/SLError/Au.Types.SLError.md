# Enum `Au.Types.SLError`

SQLite API error codes. Also two success codes - Row and Done.

```
public enum SLError
```

### Fields

| Name | Description |
| --- | --- |
| Abort | Callback routine requested an abort |
| Auth | Authorization denied |
| Busy | The database file is locked |
| CantOpen | Unable to open the database file |
| Constraint | Abort due to constraint violation |
| Corrupt | The database disk image is malformed |
| Done | `sqlite3_step` has finished executing |
| Empty | Database is empty |
| Error | SQL error or missing database |
| Format | Auxiliary database format error |
| Full | Insertion failed because database is full |
| Internal | Internal logic error in SQLite |
| Interrupt | Operation terminated by `sqlite3_interrupt` |
| IoErr | Some kind of disk I/O error occurred |
| Locked | A table in the database is locked |
| Mismatch | Data type mismatch |
| Misuse | Library used incorrectly |
| NoLfs | Uses OS features not supported on host |
| NoMem | A malloc() failed |
| NotADb | File opened that is not a database file |
| NotFound | Unknown opcode in `sqlite3_file_control` |
| Notice | Notifications from `sqlite3_log` |
| Ok | Successful result |
| Perm | Access permission denied |
| Protocol | Database lock protocol error |
| Range | 2nd parameter to `sqlite3_bind` out of range |
| ReadOnly | Attempt to write a readonly database |
| Row | `sqlite3_step` has another row ready |
| Schema | The database schema changed |
| TooBig | String or BLOB exceeds size limit |
| Warning | Warnings from `sqlite3_log` |