# Method `Au.More.StringUtil.RemoveUnderlineChar`

Removes characters used to underline next character when the text is displayed in UI. Replaces two such characters with single.

```
public static string RemoveUnderlineChar(string s, char underlineChar = '&')
```

##### Parameters

- *s*  (`string`):
    Can be `null`.
- *underlineChar*  (`char`)

##### Returns

`string`

#### Remarks

Character `'&'` (in WPF `'_'`) is used to underline next character in displayed text of dialog controls and menu items. Two such characters are used to display single. The underline is displayed when using the keyboard with `Alt` key to select dialog controls and menu items.