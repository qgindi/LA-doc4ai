# Property `Au.Types.OKey.RestoreClipboardExceptFormats`

When copying or pasting text, and `Au.Types.OKey.RestoreClipboardAllFormats` is `true`, do not restore clipboard data of these formats. Default: `null`.

```
public static string[] RestoreClipboardExceptFormats { get; set; }
```

##### Property Value

`string[]`

#### Remarks

To restore clipboard data, the copy/paste functions at first get clipboard data. Getting data of some formats set by some apps can be slow (100 ms or more) or cause problems (the app can change something in its window or even show a dialog). It also depends on whether this is the first time the data is being retrieved. The app can render data on demand, when some app is retrieving it from the clipboard first time; then can be slow etc.

You can use function `Au.Types.OKey.PrintClipboard` to see format names and get-data times.

There are several kinds of clipboard formats - registered, standard, private and display. Only registered formats have string names. For standard formats use API constant names, like `"CF_WAVE"`. Private, display and metafile formats are never restored. These formats are never restored: `CF_METAFILEPICT`, `CF_ENHMETAFILE`, `CF_PALETTE`, `CF_OWNERDISPLAY`, `CF_DSPx` formats, `CF_GDIOBJx` formats, `CF_PRIVATEx` formats. Some other formats too, but they are automatically synthesized from other formats if need. Also does not restore if data size is 0 or > 10 MB.

This property is static, not thread-static. It should be set (if need) at the start of script and not changed later.

#### Examples

```
OKey.RestoreClipboardExceptFormats = ["CF_UNICODETEXT", "HTML Format"];
```

### See Also

`Au.Types.OKey.RestoreClipboard`

`Au.Types.OKey.PrintClipboard`