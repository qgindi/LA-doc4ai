# Method `Au.keys.more.parseKeysString`

Converts keys string to `Au.Types.KKey` array.

```csharp
public static KKey[] parseKeysString(string keys_)
```

##### Parameters

- *keys_*  (`string`):
  String containing one or more [key names](🔗). Operators are not supported.

##### Returns

`Au.Types.KKey[]`

##### Exceptions

- `ArgumentException`:
  Error in *keys_* string.