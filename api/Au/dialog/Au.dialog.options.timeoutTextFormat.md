# Property `Au.dialog.options.timeoutTextFormat`

Timeout text format string. See `Au.dialog.CloseAfter`.

```
public static string timeoutTextFormat { get; set; }
```

##### Property Value

`string`

#### Remarks

Default: `"{0} s until this dialog closes, unless clicked.\nTimeout action: {1}."`. Use placeholder `{0}` for seconds (in the first line) and `{1}` for timeout action (in the second line).