# Enum `Au.Types.FPFormat`

Used with `Au.filesystem.more.getFinalPath`

```
public enum FPFormat
```

### Fields

| Name | Description |
| --- | --- |
| PrefixAlways | Always with long-path prefix (`"\\?\"` or `"\\?\UNC\"`). |
| PrefixIfLong | With long-path prefix (`"\\?\"` or `"\\?\UNC\"`) if path length > `Au.pathname.maxDirectoryPathLength`. This is default. |
| PrefixNever | Without long-path prefix, even if the path is very long. |
| VolumeGuid | With volume GUID (API `GetFinalPathNameByHandle` flag `VOLUME_NAME_GUID`). If it fails (eg network path), gets path with prefix, like `PrefixAlways`. |