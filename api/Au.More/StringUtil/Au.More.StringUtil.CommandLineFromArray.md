# Method `Au.More.StringUtil.CommandLineFromArray`

Converts array of command line arguments to string that can be passed to a "start process" function, for example `Au.run.it`, `System.Diagnostics.Process.Start`.

```
public static string CommandLineFromArray(string[] a)
```

##### Parameters

- *a*  (`string[]`)

##### Returns

`string`

`null` if *a* is `null` or empty.