# PowerShell, VBScript, Python

Run a PowerShell script and print the output. See [PowerShell.exe command line](https://www.google.com/search?q=PowerShell.exe+command+line).

```
string code1 = """
[console]::OutputEncoding = [System.Text.Encoding]::Unicode
Write-Host 'PowerShell'
""";
using var file1 = new TempFile(".ps1");
filesystem.saveText(file1, code1, encoding: Encoding.Unicode);
run.console("PowerShell.exe", $"-ExecutionPolicy Bypass -File \"{file1}\"", encoding: Encoding.Unicode);
```

Run a VBScript script and print the output. See [cscript.exe command line](https://www.google.com/search?q=cscript.exe+command+line). No Unicode output.

```
string code2 = """
Wscript.Echo "VBScript"
""";
using var file2 = new TempFile(".vbs");
filesystem.saveText(file2, code2, encoding: Encoding.Unicode);
run.console("Cscript.exe", $"/e:VBScript /nologo \"{file2}\"");
```

The same should work for JScript. Replace /e:VBScript with /e:JScript.

To run Python code from C# and vice versa can be used [Python.NET](http://pythonnet.github.io/). NuGet pythonnet. See [example](https://www.libreautomate.com/forum/showthread.php?tid=7484&pid=36975#pid36975). Need to install [Python](https://www.python.org/downloads/). Another similar library - [IronPython](https://ironpython.net/). NuGet IronPython.