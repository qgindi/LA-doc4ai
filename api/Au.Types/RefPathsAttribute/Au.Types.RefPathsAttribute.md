# Class `Au.Types.RefPathsAttribute`

The default compiler adds this attribute to the main assembly if using non-default references (meta `r` or `nuget`). Allows to find them at run time. Only if role `miniProgram` (default) or `editorExtension`.

```
[AttributeUsage(AttributeTargets.Assembly)]
public sealed class RefPathsAttribute : Attribute
```

##### Inheritance

`object` → `Attribute` → `RefPathsAttribute`

### Constructors

`RefPathsAttribute(string)`

### Fields

`Paths`