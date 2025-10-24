# Property `Au.consoleProcess.Encoding`

Console's text encoding. Default is `System.Text.Encoding.UTF8`.

```
public Encoding Encoding { get; set; }
```

##### Property Value

`Encoding`

#### Remarks

If wrong encoding, the received text may contain garbage. Try `System.Console.OutputEncoding` or `System.Text.Encoding.Unicode`.