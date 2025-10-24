# Command line programs

There are several useful [Windows command line](https://www.google.com/search?q=Windows+command+line+site%3Amicrosoft.com) programs and commands.

To run programs, use `Au.run.console`.

```
run.console("ipconfig.exe", "/flushdns");
```

To run other commands, use a `.bat` file or [cmd.exe](https://www.google.com/search?q=cmd.exe+site%3Amicrosoft.com).

```
var commands = """
cd /d C:\Test\Folder
dir
""";
commands = commands.Replace("\r\n", " && ");
run.console("cmd.exe", $"""/u /c "{commands}" """, encoding: Encoding.Unicode);
```

Also you can find command line programs on the internet, or even already have them installed.

```
string file1 = @"C:\Test\icons.db";
var file2 = @"C:\Test\icons.7z";
run.console(folders.ProgramFiles + @"7-Zip\7z.exe", $"""a "{file2}" "{file1}" """);
```

Some links:

- [Sysinternals](https://learn.microsoft.com/en-us/sysinternals/downloads/)
- [NirSoft](https://www.nirsoft.net/utils/)