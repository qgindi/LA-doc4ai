# Class `Au.Types.HSContentPart`

Contains a single part of a multipart POST data.

```csharp
public record HSContentPart : IEquatable<HSContentPart>
```

##### Inheritance

`object` → `HSContentPart`

### Constructors

`HSContentPart(int, Dictionary<string, string>, byte[])`

### Properties

`Content`, `ContentType`, `FileName`, `Headers`, `Index`, `Name`, `Text`