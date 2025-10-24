# Method `Au.opt.scope.warnings`

Creates temporary scope for `Au.opt.warnings` options. See example.

```
public static UsingEndAction warnings(bool inherit = true)
```

##### Parameters

- *inherit*  (`bool`):
    If `true` (default), inherit current options. If `false`, uses default options.

##### Returns

`Au.Types.UsingEndAction`

#### Examples

```
opt.warnings.Verbose = false;
print.it(opt.warnings.Verbose, opt.warnings.IsDisabled("Test*"));
using(opt.scope.warnings()) {
	opt.warnings.Verbose = true;
	opt.warnings.Disable("Test*");
	print.it(opt.warnings.Verbose, opt.warnings.IsDisabled("Test*"));
} //here restored automatically
print.it(opt.warnings.Verbose, opt.warnings.IsDisabled("Test*"));
```