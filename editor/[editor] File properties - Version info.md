# File properties - **Version info**

To add version info to your exe program, insert and edit this code near the start of any C# file of the compilation.

```
using System.Reflection;

[assembly: AssemblyVersion("1.0.0.0")]
//[assembly: AssemblyFileVersion("1.0.0.0")] //if missing, uses AssemblyVersion
//[assembly: AssemblyTitle("File description")]
//[assembly: AssemblyDescription("Comments")]
//[assembly: AssemblyCompany("Company name")]
//[assembly: AssemblyProduct("Product name")]
//[assembly: AssemblyInformationalVersion("1.0.0.0")] //product version
//[assembly: AssemblyCopyright("Copyright © {{DateTime.Now.Year}} ")]
//[assembly: AssemblyTrademark("Legal trademarks")]
```