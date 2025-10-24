# Create folder

Create folder (directory) if does not exist.

```
filesystem.createDirectory(@"C:\Test\Folder"); //also creates C:\Test if need
```

Create folder (if does not exist) for the specified file.

```
filesystem.createDirectoryFor(@"C:\Test\Folder\file.txt"); //creates C:\Test\Folder if need
```

If need custom security permissions, there are several ways:

- Use a folder that has these security settings as a template.
- Run [`icacls or cacls`](https://www.google.com/search?q=%60icacls+or+cacls%60) with `Au.run.console`.
- Use `DirectoryInfo.SetAccessControl` and `System.Security.AccessControl.DirectorySecurity`.

```
filesystem.createDirectory(@"C:\Test\Folder", @"C:\Template folder");
```