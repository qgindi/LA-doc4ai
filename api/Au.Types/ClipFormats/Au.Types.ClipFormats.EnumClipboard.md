# Method `Au.Types.ClipFormats.EnumClipboard`

Gets formats currently in the clipboard.

```
public static IEnumerable<int> EnumClipboard()
```

##### Returns

`IEnumerable<int>`

#### Examples

```
foreach (var f in ClipFormats.EnumClipboard()) {
	print.it(ClipFormats.GetName(f));
}
```