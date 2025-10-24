# Enum `Au.Types.FDFlags`

flags for `Au.filesystem.delete`.

```
[Flags]
public enum FDFlags
```

### Fields

| Name | Description |
| --- | --- |
| CanFail | If fails to delete, don't wait/retry and don't throw exception. |
| RecycleBin | Send to the Recycle Bin. If not possible, delete anyway, unless used `CanFail`. Why could be not possible: 1. The file is in a removable drive (most removables don't have a recycle bin). 2. The file is too large. 3. The path is too long. 4. The Recycle Bin is not used on that drive (it can be set in the Recycle Bin Properties dialog). 5. This process is non-UI-interactive, eg a service. 6. Unknown reasons. Note: it is much slower. To delete multiple, use `Au.filesystem.delete`. |