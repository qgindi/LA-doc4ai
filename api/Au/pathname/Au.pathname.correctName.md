# Method `Au.pathname.correctName`

Replaces characters that cannot be used in file names.

```
public static string correctName(string name, string invalidCharReplacement = "-")
```

##### Parameters

- *name*  (`string`):
    Initial filename.
- *invalidCharReplacement*  (`string`):
    A string that will replace each invalid character. Default `"-"`.

##### Returns

`string`

#### Remarks

Also corrects other forms of invalid or problematic filename: trims spaces and other blank characters; replaces `"."` at the end; prepends `"@"` if a reserved name like `"CON"` or `"CON.txt"`; returns `"-"` if *name* is `null`/empty/whitespace. Usually returns valid filename, however it can be too long (itself or when combined with a directory path).