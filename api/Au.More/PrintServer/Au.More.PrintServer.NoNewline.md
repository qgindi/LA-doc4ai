# Property `Au.More.PrintServer.NoNewline`

Let messages don't end with `"\r\n"`.

```
public bool NoNewline { get; set; }
```

##### Property Value

`bool`

#### Remarks

This can be used for performance, to avoid string copying when using local server. Does not affect performance of global server.