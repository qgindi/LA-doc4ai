# Property `Au.folders.SystemX64`

Gets non-redirected path of the System32 folder.

```
public static FolderPath SystemX64 { get; }
```

##### Property Value

`Au.Types.FolderPath`

#### Remarks

If this process is 32-bit and OS is 64-bit, when it uses the `Au.folders.System` folder path (`@"C:\WINDOWS\system32"`), the OS in most cases redirects it to `@"C:\Windows\SysWOW64"`, which contains 32-bit versions of program files. Use SystemX64 when you want to avoid the redirection and access the true System32 folder which on 64-bit OS contains 64-bit program files. More info in class help.

### See Also

`Au.More.FileSystemRedirection`

`Au.osVersion.is32BitProcessAnd64BitOS`