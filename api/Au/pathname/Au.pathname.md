# Class `Au.pathname`

File path string functions. Parse, combine, make full, make unique, make valid, expand variables, etc.

```
public static class pathname
```

##### Remarks

Most functions of this class work with strings and don't access the file system. Several functions query file system info.

Functions of this class don't throw exceptions when path is invalid (path format, invalid characters). Only `Au.pathname.normalize` throws exception if not full path.

Also you can use .NET class `System.IO.Path`. In its documentation you'll find more info about paths.

##### Inheritance

`object` → `pathname`

### Fields

`maxDirectoryPathLength`, `maxFilePathLength`

### Methods

`combine`, `correctName`, `expand`, `findExtension`, `getDirectory`, `getExtension`, `getExtension`, `getName`, `getNameNoExt`, `getRootLength`, `getUrlProtocolLength`, `isFullPath`, `isFullPathExpand`, `isFullPathExpand`, `isInvalidName`, `isInvalidNameChar`, `isInvalidPathChar`, `isUrl`, `makeUnique`, `normalize`, `prefixLongPath`, `prefixLongPathIfNeed`, `unprefixLongPath`