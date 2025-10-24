# .NET, NuGet, other libraries

In scripts can be used everything from .NET libraries. Don't need to add assembly references. Add just `using` directives that aren't in file `global.cs`.

```
using System.Xml.Linq;

var x = XElement.Load(@"C:\Test\file.xml");
```

Many other managed libraries can be downloaded, for example from [NuGet](https://www.google.com/search?q=NuGet) or [GitHub](https://www.google.com/search?q=GitHub+.NET+libraries). To install NuGet packages, use menu **Tools > NuGet**.

When a NuGet package or some other library is installed, need to add its reference to scripts where you want to use it. You can do it in the **NuGet** tool or in **Properties**. Then you'll find one or more new namespaces in the `Ctrl+Space` list, and can use them.

```
/*/ nuget -\Humanizer; /*/
using Humanizer;

var s = "one two";
s = s.Titleize();
print.it(s);
```

If a library has several versions for different .NET frameworks, use the newest .NET version, if available, else .NET Standard. If these are unavailable, probably the library is abandoned and should not be used. Don't use libraries for .NET Framework 4.x and older.