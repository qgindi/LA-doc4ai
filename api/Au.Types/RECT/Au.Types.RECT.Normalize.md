# Method `Au.Types.RECT.Normalize`

If `width` or `height` are negative, modifies this rectangle so that they would not be negative.

```csharp
public void Normalize(bool swap)
```

##### Parameters

- *swap*  (`bool`):
  `true` - swap `right`/`left`, `bottom`/`top`; `false` - set `right` = `left`, `bottom` = `top`.