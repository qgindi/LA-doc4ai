# Property `Au.Types.FAttr.IsNtfsLink`

It is a NTFS link, such as symbolic link, junction or mount point. Don't confuse with shell links (shortcuts). If `Au.Types.FAttr.File` `true`, the target is a file. If `Au.Types.FAttr.Directory` `true`, the target is a directory.

```
public bool IsNtfsLink { get; }
```

##### Property Value

`bool`