# Class `Au.More.ResourceUtil`

Gets managed resources from a .NET assembly.

```
public static class ResourceUtil
```

##### Remarks

Internally uses `System.Resources.ResourceManager`. Uses `System.Globalization.CultureInfo.InvariantCulture`.

Loads resources from managed resource `"AssemblyName.g.resources"`. To add such resource files in Visual Studio, set file build action = `Resource`. Don't use `.resx` files and the **Resources** page in **Project Properties**.

By default loads resources from the app entry assembly. In script with role `miniProgram` - from the script's assembly. To specify another loaded assembly, use prefix like `"<AssemblyName>"` or `"*<AssemblyName>"`.

The resource name argument can optionally start with `"resource:"`.

Does not use caching. Creates new object even when loading the resource not the first time.

##### Inheritance

`object` → `ResourceUtil`

### Methods

`GetBytes`, `GetGdipBitmap`, `GetStream`, `GetString`, `GetWpfImage`, `GetWpfImageElement`, `GetXamlObject`, `Get<T>`, `HasResourcePrefix`