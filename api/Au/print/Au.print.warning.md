# Method `Au.print.warning`

## Overload 1

Writes a warning text to the output. By default appends the stack trace.

```
public static void warning(string text, int showStackFromThisFrame = 0, string prefix = "<>Warning: ")
```

##### Parameters

- *text*  (`string`):
    Warning text.
- *showStackFromThisFrame*  (`int`):
    If >= 0, appends the stack trace, skipping this number of frames. Default 0. Does not append if *text* looks like a stack trace.
- *prefix*  (`string`):
    Text before *text*. Default `"<>Warning: "`.

#### Remarks

Calls `Au.print.it`. Does not show more than 1 warning/second, unless `opt.warnings.Verbose == true` (see `Au.Types.OWarnings.Verbose`). To disable some warnings, use code `opt.warnings.Disable("warning text wildcard");` (see `Au.Types.OWarnings.Disable`).

### See Also

`Au.Types.OWarnings`

* * *

## Overload 2

Writes an exception warning to the output.

```
public static void warning(Exception e, string prefix = "<>Warning: ")
```

##### Parameters

- *e*  (`Exception`)
- *prefix*  (`string`):
    Text before *text*. Default `"<>Warning: "`.

#### Remarks

Calls `Au.print.it`. Does not show more than 1 warning/second, unless `opt.warnings.Verbose == true` (see `Au.Types.OWarnings.Verbose`). To disable some warnings, use code `opt.warnings.Disable("warning text wildcard");` (see `Au.Types.OWarnings.Disable`).

### See Also

`Au.Types.OWarnings`