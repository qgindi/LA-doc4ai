# Property `Au.print.logFile`

Sets log file path. When set (not `null`), text passed to `Au.print.it` will be written to the file. If value is `null` - restores default behavior.

```
public static string logFile { get; set; }
```

##### Exceptions

- `ArgumentException`:
    The `set` function throws this exception if the value is not full path and not `null`.

##### Property Value

`string`

#### Remarks

The first `Au.print.it` etc call (in this process) creates or opens the file and deletes old content if the file already exists.

Also supports mailslots. Use mailslot name, as documented in `CreateMailslot`. Multiple processes can use the same mailslot.