# Property `Au.Types.OKey.TextHow`

How to send text to the active window (keys, characters or clipboard).
Default:`Au.Types.OKeyText.Characters`.

```csharp
public OKeyText TextHow { get; set; }
```

##### Property Value

`Au.Types.OKeyText`

#### Examples

```csharp
opt.key.TextHow = OKeyText.Paste;
```