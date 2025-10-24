# Property `Au.consoleProcess.IsLine`

`Au.consoleProcess.Read` sets this property = `true` if in console output the line text ended with newline characters; `false` if not.

```
public bool IsLine { get; }
```

##### Property Value

`bool`

#### Remarks

If returns `false`, the text returned by the last `Au.consoleProcess.Read` is either a prompt (incomplete line that asks for user input) or an incomplete line. You can use `Au.consoleProcess.Wait` to wait for more text.