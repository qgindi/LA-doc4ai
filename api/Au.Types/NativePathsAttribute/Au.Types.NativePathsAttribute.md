# Class `Au.Types.NativePathsAttribute`

The default compiler adds this attribute to the main assembly if using NuGet packages with native dlls. Allows to find the dlls at run time. Only if role `miniProgram` (default) or `editorExtension`.

```
[AttributeUsage(AttributeTargets.Assembly)]
public sealed class NativePathsAttribute : Attribute
```

##### Inheritance

`object` → `Attribute` → `NativePathsAttribute`

### Constructors

`NativePathsAttribute(string)`

### Fields

`Paths`