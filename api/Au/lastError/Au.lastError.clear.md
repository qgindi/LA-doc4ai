# Method `Au.lastError.clear`

Calls API `SetLastError`(0), which clears the Windows API last error code of this thread.

```
public static void clear()
```

#### Remarks

Need it before calling some functions if you want to use `Au.lastError.code` or `Au.lastError.message`. The same as `lastError.code = 0;`.