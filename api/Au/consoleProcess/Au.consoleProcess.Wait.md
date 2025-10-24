# Method `Au.consoleProcess.Wait`

Waits for more text and tells next `Au.consoleProcess.Read` to get old + new text.

```
public bool Wait(int timeout = -1)
```

##### Parameters

- *timeout*  (`int`):
    Timeout, ms. The function returns `false` if did not receive more text during that time. If -1, returns `true` without waiting (next `Au.consoleProcess.Read` will wait).

##### Returns

`bool`

`true` if received more text or if *timeout* is -1.

##### Exceptions

- `InvalidOperationException`:
    `Au.consoleProcess.IsLine` `true`. Or multiple `Au.consoleProcess.Wait(int)` without `Au.consoleProcess.Read`.

#### Remarks

If returns `true`, next `Au.consoleProcess.Read` will get the old text + new text. If the console process ends while waiting, next `Read` will get the old text, and `Au.consoleProcess.IsLine` will be `true`.