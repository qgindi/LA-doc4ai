# Method `Au.Types.ClipFormats.GetName`

Gets clipboard format name.

```
public static string GetName(int format, bool orNull = false)
```

##### Parameters

- *format*  (`int`):
    A registered or standard clipboard format. If standard, returns string like `"CF_BITMAP"`.
- *orNull*  (`bool`):
    Return `null` if *format* is unknown. If `false`, returns *format* as string.

##### Returns

`string`

#### Remarks

Calls API `GetClipboardFormatName`. Although undocumented, it also can get other strings from the same system atom table, for example registered Windows message names and window class names.