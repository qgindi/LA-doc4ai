# Method `Au.opt.scope.mouse`

Creates temporary scope for `Au.opt.mouse` options. See example.

```
public static UsingEndAction mouse(bool inherit = true)
```

##### Parameters

- *inherit*  (`bool`):
    If `true` (default), inherit current options. If `false`, uses default options.

##### Returns

`Au.Types.UsingEndAction`

#### Examples

```
print.it(opt.mouse.ClickSpeed);
using(opt.scope.mouse()) {
	opt.mouse.ClickSpeed = 100;
	print.it(opt.mouse.ClickSpeed);
} //here restored automatically
print.it(opt.mouse.ClickSpeed);
```