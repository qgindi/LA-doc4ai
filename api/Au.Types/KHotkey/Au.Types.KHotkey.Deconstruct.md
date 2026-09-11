# Method `Au.Types.KHotkey.Deconstruct`

Allows to get properties of a `Au.Types.KHotkey` variable like `var (mod, key) = hotkey;`

```csharp
public void Deconstruct(out KMod mod, out KKey key)
```

##### Parameters

- *mod*  (`Au.Types.KMod`):
  Enum: Shift, Ctrl, Alt, Win.
- *key*  (`Au.Types.KKey`)