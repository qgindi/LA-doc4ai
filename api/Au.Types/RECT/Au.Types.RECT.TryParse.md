# Method `Au.Types.RECT.TryParse`

Converts string to `Au.Types.RECT`.

```
public static bool TryParse(string s, out RECT r)
```

##### Parameters

- *s*  (`string`):
    String in format `"{L=left T=top W=width H=height}"` (`Au.Types.RECT.ToString`) or `"left top width height"` (`Au.Types.RECT.ToStringSimple`).
- *r*  (`Au.Types.RECT`)

##### Returns

`bool`

`false` if invalid string format.