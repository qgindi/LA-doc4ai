# Method `Au.opt.scope.key`

Creates temporary scope for `Au.opt.key` options. See example.

```
public static UsingEndAction key(bool inherit = true)
```

##### Parameters

- *inherit*  (`bool`):
    If `true` (default), inherit current options. If `false`, uses default options.

##### Returns

`Au.Types.UsingEndAction`

#### Examples

```
print.it(opt.key.KeySpeed);
using(opt.scope.key()) {
	opt.key.KeySpeed = 5;
	print.it(opt.key.KeySpeed);
} //here restored automatically
print.it(opt.key.KeySpeed);
```