# Method `Au.process.suspend`

## Overload 1

Suspends or resumes the specified process.

```
public static bool suspend(bool suspend, int processId)
```

##### Parameters

- *suspend*  (`bool`):
    `true` suspend, `false` resume.
- *processId*  (`int`):
    Process id.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

#### Remarks

If suspended multiple times, must be resumed the same number of times.

* * *

## Overload 2

Suspends or resumes all processes of the specified program or programs.

```
public static int suspend(bool suspend, string processName, bool allSessions = false)
```

##### Parameters

- *suspend*  (`bool`):
    `true` suspend, `false` resume.
- *processName*  (`string`):
    Process executable file name (like `"notepad.exe"`) or full path. String format: [wildcard expression](../articles/Wildcard%20expression.html).
- *allSessions*  (`bool`):
    Processes of any user session. If `false` (default), only processes of this user session.

##### Returns

`int`

The number of successfully suspended/resumed processes.

##### Exceptions

- `ArgumentException`:

    - *processName* is `""` or `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).

#### Remarks

If suspended multiple times, must be resumed the same number of times.