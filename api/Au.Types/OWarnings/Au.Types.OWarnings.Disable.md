# Method `Au.Types.OWarnings.Disable`

Disables one or more run-time warnings.

```
public UsingEndAction Disable(params string[] warningsWild)
```

##### Parameters

- *warningsWild*  (`string[]`):
    One or more warnings as case-insensitive wildcard strings. See `Au.Types.ExtString.Like`.

##### Returns

`Au.Types.UsingEndAction`

#### Remarks

Adds the strings to an internal list. When `Au.print.warning` is called, it looks in the list. If finds the warning in the list, does not show the warning. It's easy to auto-restore warnings with `using`, like in the second example. Restoring is optional.

#### Examples

```
opt.warnings.Disable("*part of warning 1 text*", "*part of warning 2 text*");
```

Temporarily disable all warnings.

```
opt.warnings.Verbose = true;
print.warning("one");
using(opt.warnings.Disable("*")) {
	print.warning("two");
}
print.warning("three");
```