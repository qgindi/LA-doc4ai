# Property `Au.print.redirectConsoleOutput`

Let `Console.WriteX` methods in non-console process write to the same destination as `Au.print.it`.

```
public static bool redirectConsoleOutput { get; set; }
```

##### Property Value

`bool`

#### Remarks

The default value is `true` in non-console scripts that use class `System.Console` and have role `miniProgram` (default); also `exeProgram` if started from the script editor. Also in these scripts `Console.ReadLine` uses `Au.dialog.showInput`.

If `Console.Write` text does not end with `'\n'` character, it is buffered and not displayed until called again with text ending with `'\n'` character or until called `Console.WriteLine`.

`Console.Clear` will not clear output; it will throw exception.