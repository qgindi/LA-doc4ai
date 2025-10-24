# Method `Au.More.FileWatcher.Watch`

Starts watching a file for external changes. An external change is when another process writes, creates, deletes, moves or renames the file.

```
public static FileWatcher Watch(string file, Action onExternalChange)
```

##### Parameters

- *file*  (`string`):
    Full path of a file, without environment variables.
- *onExternalChange*  (`Action`):
    Called when detected that the file was changed externally. Important: when your app writes, creates, deletes, moves or renames the file, it must set `Au.More.FileWatcher.Paused` = `true` during the file operation. Runs in a thread pool thread.

##### Returns

`Au.More.FileWatcher`

A new `Au.More.FileWatcher` instance used to manage the watcher. Don't need to dispose it, unless you want to stop watching before the process exits. Returns `null` and prints a warning if the watcher could not be created (for example the directory does not exist).

##### Exceptions

- `NotSupportedException`:
    Thrown if this method has already been called for the same file without a corresponding call to `Au.More.FileWatcher.Dispose`. If multiple notification handlers are needed, combine them into the *onExternalChange* delegate.

#### Examples

`Au.More.FileWatcher`