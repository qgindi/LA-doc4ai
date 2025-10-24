# Method `Au.More.ScriptEditor.GetIcon`

Gets icon string in specified format.

```
public static string GetIcon(string file, EGetIcon what)
```

##### Parameters

- *file*  (`string`):
    Script file/folder path etc, or icon name. See `Au.Types.EGetIcon`, `Au.More.ImageUtil.LoadWpfImageElement`.
- *what*  (`Au.Types.EGetIcon`):
    The format of input and output strings.

##### Returns

`string`

Returns `null` if editor isn't running or if the file does not exist. Read more in Remarks.

#### Remarks

If *what* is `Au.Types.EGetIcon.IconNameToXaml`, this function tries to get icon XAML from assembly resources (passes *file* to `Au.More.ResourceUtil.GetString`, with color removed); if not found - from editor. By default the LibreAutomate compiler finds literal icon-like strings in code and adds icon XAML to assembly resources; see **Properties > Resource > Options**.