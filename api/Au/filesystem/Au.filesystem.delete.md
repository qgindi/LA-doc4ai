# Method `Au.filesystem.delete`

## Overload 1

Deletes file or directory if exists.

```
public static bool? delete(string path, FDFlags flags = 0)
```

##### Parameters

- *path*  (`string`):
    Full path.
- *flags*  (`Au.Types.FDFlags`)

##### Returns

`bool?`

`true` if deleted, `false` if failed (with flag `CanFail`), `null` if did not exist.

##### Exceptions

- `ArgumentException`:
    *path* is not full path (see `Au.pathname.isFullPath`).
- `Au.Types.AuException`:
    Failed.

#### Remarks

Does nothing if it does not exist (no exception). If directory, also deletes all its files and subdirectories. If fails to delete some, tries to delete as many as possible. Deletes read-only files too. Does not show any message boxes etc (confirmation, error, UAC consent, progress).

Some reasons why this function can fail:

1. The file is open (in any process). Or a file in the directory is open.
2. This process does not have security permissions to access or delete the file or directory or some of its descendants.
3. The directory is (or contains) the "current directory" (in any process).

* * *

## Overload 2

Deletes multiple files or/and directories.

```
public static bool? delete(IEnumerable<string> paths, FDFlags flags = 0)
```

##### Parameters

- *paths*  (`IEnumerable<string>`):
    string array, `List` or other collection. Full paths.
- *flags*  (`Au.Types.FDFlags`)

##### Returns

`bool?`

`true` if deleted all, `false` if failed to delete all or some (with flag `CanFail`), `null` if none existed.

##### Exceptions

- `ArgumentException`:
    *path* is not full path (see `Au.pathname.isFullPath`).
- `AggregateException`:
    Failed to delete all or some items. The exception object contains one `Au.Types.AuException` for each failed-to-delete item.

#### Remarks

This overload is faster when using Recycle Bin. If fails to delete some items specified in the list, deletes as many as possible.