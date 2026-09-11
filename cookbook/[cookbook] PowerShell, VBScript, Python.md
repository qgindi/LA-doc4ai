# PowerShell, VBScript, Python

Run a PowerShell script and print the output. See [PowerShell.exe command line](🔗).

```csharp
string code1 = """
[console]::OutputEncoding = [System.Text.Encoding]::Unicode
Write-Host 'PowerShell'
""";
using var file1 = new TempFile(".ps1");
filesystem.saveText(file1, code1, encoding: Encoding.Unicode);
run.console("PowerShell.exe", $"-ExecutionPolicy Bypass -File \"{file1}\"", encoding: Encoding.Unicode);
```

Run a VBScript script and print the output. See [cscript.exe command line](🔗). No Unicode output.

```csharp
string code2 = """
Wscript.Echo "VBScript"
""";
using var file2 = new TempFile(".vbs");
filesystem.saveText(file2, code2, encoding: Encoding.Unicode);
run.console("Cscript.exe", $"/e:VBScript /nologo \"{file2}\"");
```

The same should work for JScript. Replace /e:VBScript with /e:JScript.

To run Python code from C# and vice versa can be used [Python.NET](🔗). NuGet pythonnet. See [example](https://www.libreautomate.com/forum/showthread.php?tid=7484&pid=36975). Need to install [Python](🔗).
Another similar library -[IronPython](🔗). NuGet IronPython.