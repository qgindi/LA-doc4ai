# Struct `Au.Types.MTImage`

Used for menu/toolbar function parameters to specify an image in different ways (file path, `System.Drawing.Image` object, etc).

```
public struct MTImage
```

##### Remarks

Has implicit conversions from string, `System.Drawing.Image`, `Au.icon`, `Au.Types.StockIcon`, `Au.Types.FolderPath`. More info: `Au.Types.MTBase`.

### Properties

`Value`

### Operators

`implicit operator MTImage(FolderPath)`, `implicit operator MTImage(StockIcon)`, `implicit operator MTImage(icon)`, `implicit operator MTImage(Image)`, `implicit operator MTImage(string)`