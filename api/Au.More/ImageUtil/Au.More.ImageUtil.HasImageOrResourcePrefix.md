# Method `Au.More.ImageUtil.HasImageOrResourcePrefix`

Returns `true` if string starts with `"resource:"`, `"resources/"`, `"image:"` (Base64 encoded image), `"imagefile:"` (file path), `"*"` (XAML icon name) or `"<"` (possibly XAML image).

```
public static bool HasImageOrResourcePrefix(string s)
```

##### Parameters

- *s*  (`string`)

##### Returns

`bool`