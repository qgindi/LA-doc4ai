# Method `Au.consoleProcess.ReadLine`

Waits and reads next full line.

```
public bool ReadLine(out string s)
```

##### Parameters

- *s*  (`string`):
    Receives the text. It does not contain newline characters (`'\r'`, `'\n'`).

##### Returns

`bool`

`false` if there is no more text to read because the console process ended or is ending.

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Remarks

Waits for new text from console, reads it into an internal buffer, and then returns it one full line at a time.

To read a prompt (incomplete line that asks for user input), use `Au.consoleProcess.Read` instead. This function would just hang waiting for full line ending with newline characters.