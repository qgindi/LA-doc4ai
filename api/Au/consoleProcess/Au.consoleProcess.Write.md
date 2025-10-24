# Method `Au.consoleProcess.Write`

Sends text to the console's input. Also sends character `'\n'` (like key `Enter`), unless *text* ends with `'\n'` or *noNL* is `true`.

```
public void Write(string text, bool noNL = false)
```

##### Parameters

- *text*  (`string`)
- *noNL*  (`bool`):
    Don't append character `'\n'` when *text* does not end with `'\n'`.

##### Exceptions

- `Au.Types.AuException`:
    Failed.