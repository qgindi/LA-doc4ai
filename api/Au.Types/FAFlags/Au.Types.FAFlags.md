# Enum `Au.Types.FAFlags`

Flags for `Au.filesystem.getAttributes` and some other functions.

```
[Flags]
public enum FAFlags
```

### Fields

| Name | Description |
| --- | --- |
| DontThrow | If failed, return `false` and don't throw exception. Then, if you need error info, you can use `Au.lastError`. If the file/directory does not exist, it will return `ERROR_FILE_NOT_FOUND` or `ERROR_PATH_NOT_FOUND` or `ERROR_NOT_READY`. If failed and the native error code is `ERROR_ACCESS_DENIED` or `ERROR_SHARING_VIOLATION`, the returned attributes will be `(FileAttributes)(-1)`. The file probably exists but is protected so that this process cannot access and use it. Else attributes will be 0. |
| UseRawPath | Pass path to the API as it is, without any normalizing and validating. |