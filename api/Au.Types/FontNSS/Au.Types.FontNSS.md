# Class `Au.Types.FontNSS`

Font name, size and style. If `Name` not set, will be used standard GUI font; then `Size` can be 0 to use size of standard GUI font. On high-DPI screen the font size will be scaled.

```
public record FontNSS : IEquatable<FontNSS>
```

##### Inheritance

`object` → `FontNSS`

### Constructors

`FontNSS(int, string, bool, bool)`