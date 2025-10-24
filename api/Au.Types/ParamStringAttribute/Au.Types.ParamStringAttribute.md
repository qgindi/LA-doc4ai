# Class `Au.Types.ParamStringAttribute`

A function parameter with this attribute is a string of the specified format, for example regular expression. Code editors should help to create correct string arguments: provide tools or reference, show errors.

```
[AttributeUsage(AttributeTargets.Parameter, AllowMultiple = false)]
public sealed class ParamStringAttribute : Attribute
```

##### Inheritance

`object` → `Attribute` → `ParamStringAttribute`

### Constructors

`ParamStringAttribute(PSFormat)`

### Properties

`Format`