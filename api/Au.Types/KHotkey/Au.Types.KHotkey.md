# Struct `Au.Types.KHotkey`

Defines a hotkey as `Au.Types.KMod` and `Au.Types.KKey`. Has implicit conversion operators from string like `"Ctrl+Shift+K"`, tuple `(KMod, KKey)`, enum `Au.Types.KKey`, enum `Keys`.

```
public struct KHotkey
```

### Constructors

`KHotkey(KMod, KKey)`

### Properties

`Key`, `Mod`

### Methods

`Deconstruct`, `ToString`

### Operators

`explicit operator Keys(KHotkey)`, `implicit operator KHotkey(KKey)`, `implicit operator KHotkey(string)`, `implicit operator KHotkey((KMod, KKey))`, `implicit operator KHotkey(Keys)`