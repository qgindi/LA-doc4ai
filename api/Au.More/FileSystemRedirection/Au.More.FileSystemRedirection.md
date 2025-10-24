# Struct `Au.More.FileSystemRedirection`

File system redirection functions. Can temporarily disable redirection, to allow this 32-bit process access the 64-bit System32 directory. Example: `using (FileSystemRedirection r1 = new()) { r1.Disable(); ... }`.

```
public struct FileSystemRedirection : IDisposable
```

### Methods

`Disable`, `Dispose`, `GetNonRedirectedSystemPath`, `IsSystem64PathIn32BitProcess`, `Revert`