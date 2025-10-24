# Struct `Au.Types.KKeyScan`

Virtual-key code, scan code and extended-key flag for `Au.keys.send` and similar functions.

```
public struct KKeyScan
```

##### Examples

This script prints properties of pressed keys.

```
using var hook = WindowsHook.Keyboard(k=> {
	if(!k.IsUp) print.it(k.Key, k.vkCode, k.scanCode, k.IsExtended);
}, ignoreAuInjected: false);
dialog.show("Hook");
```

### Constructors

`KKeyScan(KKey, bool)`, `KKeyScan(KKey, ushort, bool)`, `KKeyScan(ushort, bool)`

### Fields

`extendedKey`, `scanCode`, `vk`