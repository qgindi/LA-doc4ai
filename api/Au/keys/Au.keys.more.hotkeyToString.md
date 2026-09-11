# Method `Au.keys.more.hotkeyToString`

## Overload 1

Formats hotkey string like `"Ctrl+Shift+K"`.

```csharp
public static void hotkeyToString(StringBuilder b, KMod mod, KKey key)
```

##### Parameters

- *b*  (`StringBuilder`):
  Append to this `StringBuilder`.
- *mod*  (`Au.Types.KMod`):
  Enum: Shift, Ctrl, Alt, Win.
- *key*  (`Au.Types.KKey`)

* * *

## Overload 2

Formats hotkey string like `"Ctrl+Shift+K"`.

```csharp
public static string hotkeyToString(KMod mod, KKey key)
```

##### Parameters

- *mod*  (`Au.Types.KMod`):
  Enum: Shift, Ctrl, Alt, Win.
- *key*  (`Au.Types.KKey`)

##### Returns

`string`