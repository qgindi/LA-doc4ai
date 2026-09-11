# Method `Au.keys.AddKeys`

Adds keystrokes to the internal collection. They will be sent by `Au.keys.SendNow`.

```csharp
public keys AddKeys(string keys_)
```

##### Parameters

- *keys_*  (`string`):
  [Key names and operators](🔗), like with `Au.keys.send`. Can be `null` or `""`.
  Example:`"Tab Ctrl+V Alt+(E P) Left*3 Space a , 5 #5"`.
  If has prefix`"!"` or `"%"`, calls `Au.keys.AddText`; use `"!"` for text, `"%"` for HTML.

##### Returns

`Au.keys`

This.

##### Exceptions

- `ArgumentException`:
  Error in *keys_* string, for example an unknown key name.