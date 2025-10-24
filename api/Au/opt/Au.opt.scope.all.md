# Method `Au.opt.scope.all`

Creates temporary scope for all options. See example.

```
public static UsingEndAction all(bool inherit = true)
```

##### Parameters

- *inherit*  (`bool`):
    If `true` (default), inherit current options. If `false`, uses default options.

##### Returns

`Au.Types.UsingEndAction`

#### Examples

```
print.it(opt.key.KeySpeed, opt.mouse.ClickSpeed);
using(opt.scope.all()) {
	opt.key.KeySpeed = 5;
	opt.mouse.ClickSpeed = 50;
	print.it(opt.key.KeySpeed, opt.mouse.ClickSpeed);
} //here restored automatically
print.it(opt.key.KeySpeed, opt.mouse.ClickSpeed);
```