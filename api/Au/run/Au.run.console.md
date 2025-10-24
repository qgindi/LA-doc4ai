# Method `Au.run.console`

## Overload 1

Runs a console program in hidden mode, waits until its process ends, and prints its output text. Writes text lines to the output in real time.

```
public static int console(string exe, string args = null, string curDir = null, Encoding encoding = null)
```

##### Parameters

- *exe*  (`string`):

    Path or name of an `.exe` or `.bat` file. Can be:

    - Full path. Examples: `@"C:\folder\x.exe"`, `folders.System + "x.exe"`, `@"%folders.System%\x.exe"`.
    - Filename, like `"x.exe"`. This function calls `Au.filesystem.searchPath`.
    - Path relative to `Au.folders.ThisApp`. Examples: `"x.exe"`, `@"subfolder\x.exe"`, `@".\subfolder\x.exe"`, `@"..\folder\x.exe"`.

Supports environment variables, like `@"%TMP%\x.bat"`. See `Au.pathname.expand`.
- *args*  (`string`):
    `null` or command line arguments.
- *curDir*  (`string`):

    Initial current directory of the new process.

    - If `null`, uses `Directory.GetCurrentDirectory()`.
    - Else if `""`, calls `pathname.getDirectory(exe)`.
    - Else calls `Au.pathname.expand`.
- *encoding*  (`Encoding`):
    Console's text encoding. If `null` (default), uses `System.Text.Encoding.UTF8`. If you get garbage text, try `System.Console.OutputEncoding` or `System.Text.Encoding.Unicode`.

##### Returns

`int`

The process exit code. Usually a non-0 value means error.

##### Exceptions

- `Au.Types.AuException`:
    Failed, for example file not found.

#### Remarks

The console window is hidden. The text that would be displayed in it is redirected to this function.

Console programs have two output text streams - standard output and standard error. This function gets both. Alternatively use `System.Diagnostics.Process.Start`; it gets the output and error streams separately, and some lines may be received in incorrect order in time.

#### Examples

```
string v = "example";
run.console(@"C:\Test\console.exe", $@"/an ""{v}"" /etc");
```

* * *

## Overload 2

Runs a console program in hidden mode, waits until its process ends, and gets its output text.

```
public static int console(out string output, string exe, string args = null, string curDir = null, Encoding encoding = null)
```

##### Parameters

- *output*  (`string`):
    A variable that receives the output text.
- *exe*  (`string`):

    Path or name of an `.exe` or `.bat` file. Can be:

    - Full path. Examples: `@"C:\folder\x.exe"`, `folders.System + "x.exe"`, `@"%folders.System%\x.exe"`.
    - Filename, like `"x.exe"`. This function calls `Au.filesystem.searchPath`.
    - Path relative to `Au.folders.ThisApp`. Examples: `"x.exe"`, `@"subfolder\x.exe"`, `@".\subfolder\x.exe"`, `@"..\folder\x.exe"`.

Supports environment variables, like `@"%TMP%\x.bat"`. See `Au.pathname.expand`.
- *args*  (`string`):
    `null` or command line arguments.
- *curDir*  (`string`):

    Initial current directory of the new process.

    - If `null`, uses `Directory.GetCurrentDirectory()`.
    - Else if `""`, calls `pathname.getDirectory(exe)`.
    - Else calls `Au.pathname.expand`.
- *encoding*  (`Encoding`):
    Console's text encoding. If `null` (default), uses `System.Text.Encoding.UTF8`. If you get garbage text, try `System.Console.OutputEncoding` or `System.Text.Encoding.Unicode`.

##### Returns

`int`

The process exit code. Usually a non-0 value means error.

##### Exceptions

- `Au.Types.AuException`:
    Failed, for example file not found.

#### Remarks

The console window is hidden. The text that would be displayed in it is redirected to this function.

Console programs have two output text streams - standard output and standard error. This function gets both. Alternatively use `System.Diagnostics.Process.Start`; it gets the output and error streams separately, and some lines may be received in incorrect order in time.

#### Examples

```
run.console(out var text, @"C:\Test\console.exe", encoding: Console.OutputEncoding);
print.it(text);
```

* * *

## Overload 3

Runs a console program in hidden mode, waits until its process ends, and gets its output text. Uses a callback function that receives text lines in real time.

```
public static int console(Action<string> output, string exe, string args = null, string curDir = null, Encoding encoding = null, bool rawText = false)
```

##### Parameters

- *output*  (`Action<string>`):

    Callback function that receives the output text. Unless *rawText* `true`:

    - it isn't called until is retrieved full line with line break characters;
    - it receives single full line at a time, without line break characters.
- *exe*  (`string`):

    Path or name of an `.exe` or `.bat` file. Can be:

    - Full path. Examples: `@"C:\folder\x.exe"`, `folders.System + "x.exe"`, `@"%folders.System%\x.exe"`.
    - Filename, like `"x.exe"`. This function calls `Au.filesystem.searchPath`.
    - Path relative to `Au.folders.ThisApp`. Examples: `"x.exe"`, `@"subfolder\x.exe"`, `@".\subfolder\x.exe"`, `@"..\folder\x.exe"`.

Supports environment variables, like `@"%TMP%\x.bat"`. See `Au.pathname.expand`.
- *args*  (`string`):
    `null` or command line arguments.
- *curDir*  (`string`):

    Initial current directory of the new process.

    - If `null`, uses `Directory.GetCurrentDirectory()`.
    - Else if `""`, calls `pathname.getDirectory(exe)`.
    - Else calls `Au.pathname.expand`.
- *encoding*  (`Encoding`):
    Console's text encoding. If `null` (default), uses `System.Text.Encoding.UTF8`. If you get garbage text, try `System.Console.OutputEncoding` or `System.Text.Encoding.Unicode`.
- *rawText*  (`bool`):
    Call the callback function whenever text is retrieved (don't wait for full line). Pass raw text, in chunks of any size.

##### Returns

`int`

The process exit code. Usually a non-0 value means error.

##### Exceptions

- `Au.Types.AuException`:
    Failed, for example file not found.

#### Remarks

The console window is hidden. The text that would be displayed in it is redirected to this function.

Console programs have two output text streams - standard output and standard error. This function gets both. Alternatively use `System.Diagnostics.Process.Start`; it gets the output and error streams separately, and some lines may be received in incorrect order in time.

#### Examples

```
run.console(s => print.it(s), @"C:\Test\console.exe");

run.console(s => { print.it($"<><_>{s}</_><nonl>"); }, @"C:\Test\console.exe", rawText: true);
```

### See Also

`Au.consoleProcess`