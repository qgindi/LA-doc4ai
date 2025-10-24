# Property `Au.print.redirectDebugOutput`

Let `System.Diagnostics.Debug.Write`, `System.Diagnostics.Trace.Write` and similar methods also write to the same destination as `Au.print.it`.

```
public static bool redirectDebugOutput { get; set; }
```

##### Property Value

`bool`

#### Remarks

Does not replace existing `Debug.Write` etc destinations, just add new destination.

If `Debug.Write` etc argument text does not end with `'\n'` character, it is buffered and not displayed until called again with text ending with `'\n'` character or until called `Debug.WriteLine` etc.

Tip: To write to the output window even in console process, set `print.ignoreConsole=true;` before calling this method first time.