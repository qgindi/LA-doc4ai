# Method `Au.pathname.combine`

Combines two path parts using character `'\\'`. For example directory path and file name.

```
public static string combine(string s1, string s2, bool s2CanBeFullPath = false, bool prefixLongPath = true)
```

##### Parameters

- *s1*  (`string`):
    First part. Usually a directory.
- *s2*  (`string`):
    Second part. Usually a filename or relative path.
- *s2CanBeFullPath*  (`bool`):
    *s2* can be full path. If it is, ignore *s1* and return *s2* with expanded environment variables. If `false` (default), simply combines *s1* and *s2*.
- *prefixLongPath*  (`bool`):
    Call `Au.pathname.prefixLongPathIfNeed` which may prepend `@"\\?\"` if the result path is very long. Default `true`.

##### Returns

`string`

#### Remarks

If *s1* and *s2* are `null` or `""`, returns `""`. Else if *s1* is `null` or `""`, returns *s2*. Else if *s2* is `null` or `""`, returns *s1*. Does not expand environment variables. For it use `Au.pathname.expand` before, or `Au.pathname.normalize` instead. Path that starts with an environment variable here is considered not full path. Similar to `System.IO.Path.Combine`. Main differences: has some options; supports `null` arguments.

### See Also

`Au.pathname.normalize`