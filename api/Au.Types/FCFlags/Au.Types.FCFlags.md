# Enum `Au.Types.FCFlags`

flags for `Au.filesystem.copy` and some other similar functions. Used only when copying directory.

```
[Flags]
public enum FCFlags
```

### Fields

| Name | Description |
| --- | --- |
| IgnoreInaccessible | If fails to get the contents of the directory or a subdirectory because of its security settings, don't throw exception but assume that the [sub]directory is empty. |
| NoEmptyDirectories | Don't create subdirectories that after applying all filters would be empty. |
| SkipHiddenSystem | Skip descendant files and directories that have `Hidden` and `System` attributes (both). They usually are created and used only by the operating system. Drives usually have several such directories. Another example - thumbnail cache files. They often are protected and would fail to copy, ruining whole copy operation. Without this flag the function skips only these hidden-system root directories when enumerating a drive: `$Recycle.Bin`, `System Volume Information`, `Recovery`. |