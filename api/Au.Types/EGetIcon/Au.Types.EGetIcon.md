# Enum `Au.Types.EGetIcon`

For `Au.More.ScriptEditor.GetIcon`.

```
public enum EGetIcon
```

### Fields

| Name | Description |
| --- | --- |
| IconNameToXaml | Input is icon name, like `"*Pack.Icon color"`. See `Au.More.ImageUtil.LoadWpfImageElement`. Output must be icon XAML. |
| PathToIconName | Input is a file or folder in current workspace. Can be relative path in workspace (like `@"\Folder\File.cs"`) or full path or filename. Output must be icon name, like `"*Pack.Icon color"`. See `Au.More.ImageUtil.LoadWpfImageElement`. |
| PathToIconXaml | Input is a file or folder in current workspace (see `PathToIconName`). Output must be icon XAML. |