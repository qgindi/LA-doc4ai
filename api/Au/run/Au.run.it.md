# Method `Au.run.it`

Runs/opens a program, document, directory (folder), URL, new email, etc.

```
public static RResult it(string file, string args = null, RFlags flags = 0, ROptions dirEtc = null)
```

##### Parameters

- *file*  (`string`):

    Examples:

    - `@"C:\file.txt"`
    - `folders.Documents`
    - `folders.System + "notepad.exe"`
    - `@"%folders.System%\notepad.exe"`
    - `@"%TMP%\file.txt"`
    - `"notepad.exe"`
    - `@"..\folder\x.exe"`
    - `"http://a.b.c/d"`
    - `"file:///path"`
    - `"mailto:a@b.c"`
    - `":: ITEMIDLIST"`
    - `@"shell:::{CLSID}"`
    - `@"shell:AppsFolder\Microsoft.WindowsCalculator_8wekyb3d8bbwe!App"`.
- *args*  (`string`):
    Command line arguments. This function expands environment variables if starts with `"%"` or `"\"%"`.
- *flags*  (`Au.Types.RFlags`)
- *dirEtc*  (`Au.Types.ROptions`):
    Allows to specify more parameters: current directory, verb, etc. If string, it sets initial current directory for the new process. If `""`, gets it from *file*. More info: `Au.Types.ROptions.CurrentDirectory`.

##### Returns

`Au.Types.RResult`

Process info (id etc).

##### Exceptions

- `ArgumentException`:
    Used both `Au.Types.ROptions.Verb` and `Au.Types.RFlags.Admin` and this process isn't admin.
- `Au.Types.AuException`:
    Failed. For example, the file does not exist.

#### Remarks

It works like when you double-click a file icon. It may start new process or not. For example it may just activate window if the program is already running. Uses API `ShellExecuteEx`. Similar to `System.Diagnostics.Process.Start`.

The *file* parameter can be:

- Full path of a file or directory. Examples: `@"C:\file.txt"`, `folders.Documents`, `folders.System + "notepad.exe"`, `@"%folders.System%\notepad.exe"`.
- Filename of a file or directory, like `"notepad.exe"`. The function calls `Au.filesystem.searchPath`.
- Path relative to `Au.folders.ThisApp`. Examples: `"x.exe"`, `@"subfolder\x.exe"`, `@".\subfolder\x.exe"`, `@"..\another folder\x.exe"`.
- URL. Examples: `"https://www.example.com"`, `"file:///path"`.
- Email, like `"mailto:a@b.c"`. Subject, body etc also can be specified, and Google knows how.
- Shell object's `ITEMIDLIST` like `":: ITEMIDLIST"`. See `Au.Types.Pidl.ToHexString`, `Au.folders.shell`. Can be used to open virtual folders and items like Control Panel.
- Shell object's parsing name, like `@"shell:::{CLSID}"` or `@"::{CLSID}"`. See `Au.Types.Pidl.ToShellString`. Can be used to open virtual folders and items like Control Panel.
- To run a Windows Store App, use `@"shell:AppsFolder\WinStoreAppId"` format. Example: `@"shell:AppsFolder\Microsoft.WindowsCalculator_8wekyb3d8bbwe!App"`. To discover the string use hotkey `Ctrl+Shift+Q` or function `Au.More.WndUtil.GetWindowsStoreAppId` or Google.
- To open a Windows Settings page can be used [ms-settings](https://www.google.com/search?q=ms-settings), like `"ms-settings:display"`. To open Settings use `"ms-settings:"`.

Supports environment variables, like `@"%TMP%\file.txt"`. See `Au.pathname.expand`.

By default the new process isn't admin even if this process is admin. It's a unique feature of this function. More info: `Au.Types.RFlags`.

The new process inherits environment variables of this process only if both processes are admin or non-admin. To ensure it, use flag `Au.Types.RFlags.InheritAdmin` or some other "start process" function (`System.Diagnostics.Process.Start`, `Au.run.console`, Windows API).

#### Examples

Run Notepad and wait for an active Notepad window.

```
run.it("notepad.exe");
1.s();
wnd w = wnd.wait(10, true, "*- Notepad", "Notepad");
```

Run Notepad or activate a Notepad window.

```
wnd w = wnd.findOrRun("*- Notepad", run: () => run.it("notepad.exe"));
```

Run File Explorer and wait for new folder window. Ignores matching windows that already existed.

```
var w = wnd.runAndFind(
	() => run.it(@"explorer.exe"),
	10, cn: "CabinetWClass");
```

### See Also

`Au.wnd.find`

`Au.wnd.findOrRun`

`Au.wnd.runAndFind`