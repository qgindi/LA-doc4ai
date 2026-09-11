# Command line programs

There are several useful [Windows command line](🔗) programs and commands.

To run programs, use `Au.run.console`.

```csharp
run.console("ipconfig.exe", "/flushdns");
```

To run other commands, use a `.bat` file or [cmd.exe](🔗).

```csharp
var commands = """
cd /d C:\Test\Folder
dir
""";
commands = commands.Replace("\r\n", " && ");
run.console("cmd.exe", $"""/u /c "{commands}" """, encoding: Encoding.Unicode);
```

Also you can find command line programs on the internet, or even already have them installed.

```csharp
string file1 = @"C:\Test\icons.db";
var file2 = @"C:\Test\icons.7z";
run.console(folders.ProgramFiles + @"7-Zip\7z.exe", $"""a "{file2}" "{file1}" """);
```

Some links:

- [Sysinternals](🔗)
- [NirSoft](🔗)