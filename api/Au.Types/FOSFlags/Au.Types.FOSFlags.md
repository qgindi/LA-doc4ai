# Enum `Au.Types.FOSFlags`

`Au.More.FileOpenSaveDialog.CommonFlags`.

```
[Flags]
public enum FOSFlags : uint
```

### Fields

| Name | Description |
| --- | --- |
| AddToRecent | Add the selected file to recent documents. See API `SHAddToRecentDocs`. |
| NoDereferenceLinks | Shortcuts should not be treated as their target items, allowing an application to open a `.lnk` file. |
| NoValidateAccess | Do not check for situations that would prevent an application from opening the selected file, such as sharing violations or access denied errors. |
| ShowHidden | Show hidden and system items. |