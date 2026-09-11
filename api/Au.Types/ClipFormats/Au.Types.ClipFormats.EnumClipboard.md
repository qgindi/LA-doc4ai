# Method `Au.Types.ClipFormats.EnumClipboard`

Gets formats currently in the clipboard.

```csharp
public static IEnumerable<int> EnumClipboard()
```

##### Returns

`IEnumerable<int>`

#### Examples

```csharp
foreach (var f in ClipFormats.EnumClipboard()) {
	print.it(ClipFormats.GetName(f));
}
```