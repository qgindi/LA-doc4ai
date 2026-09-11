# Method `Au.keys.more.parseKeyName`

## Overload 1

Converts key name to `Au.Types.KKey`.

```csharp
public static KKey parseKeyName(string keyName)
```

##### Parameters

- *keyName*  (`string`):
  [Key name](🔗).

##### Returns

`Au.Types.KKey`

0 if unknown key name.

* * *

## Overload 2

Converts key name to `Au.Types.KKey`.

```csharp
public static KKey parseKeyName(string s, int startIndex, int length)
```

##### Parameters

- *s*  (`string`):
  String containing [key name](🔗).
- *startIndex*  (`int`):
  Key name start index in *s*.
- *length*  (`int`):
  Key name length.

##### Returns

`Au.Types.KKey`

0 if unknown key name.

##### Exceptions

- `ArgumentOutOfRangeException`:
  Invalid *startIndex* or *length*.