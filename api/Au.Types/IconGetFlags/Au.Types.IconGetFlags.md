# Enum `Au.Types.IconGetFlags`

Flags for `Au.icon.of` and similar functions.

```
[Flags]
public enum IconGetFlags
```

### Fields

| Name | Description |
| --- | --- |
| DontSearch | Don't call `Au.filesystem.searchPath`. |
| LiteralPath | The *file* argument is literal full path. Don't parse `"path,index"`, don't support `".ext"` (file type icon), don't make fully-qualified, etc. |