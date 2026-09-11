# Class `Au.Types.ExtString`

Adds extension methods for `System.String`.

```csharp
public static class ExtString
```

##### Remarks

Some .NET `System.String` methods use `System.StringComparison.CurrentCulture`by default, while others use ordinal or invariant comparison. It is confusing (difficult to remember), dangerous (easy to make bugs), slower and rarely useful.
Microsoft recommends to specify`System.StringComparison.Ordinal` `System.StringComparison.OrdinalIgnoreCase`. See [Best practices for comparing strings in .NET](🔗).
This class adds ordinal comparison versions of these methods. Same or similar name, for example`Ends` for `EndsWith`.
See also`Au.process.thisProcessCultureIsInvariant`.

This class also adds more methods.
You also can find string functions in other classes of this library, including`Au.More.StringUtil`, `Au.regexp`, `Au.pathname`, `Au.csvTable`, `Au.keys.more`, `Au.More.Convert2`, Hash.

##### Inheritance

`object` → `ExtString`

### Methods

`Ends`, `Ends`, `Ends`, `Eq`, `Eq`, `Eq`, `Eq`, `Eq`, `Eq`, `Eq`, `Eq`, `Eq`, `Eqi`, `Eqi`, `Escape`, `Find`, `Find`, `Find`, `FindAny`, `FindLastAny`, `FindLastNot`, `FindNot`, `FindWord`, `Insert`, `IsAscii`, `IsAscii`, `IsAscii`, `IsNull`, `IsNull`, `Lenn`, `Like`, `Like`, `Like`, `Limit`, `LineCount`, `LineCount`, `Lines`, `Lines`, `Lines`, `Lower`, `NE`, `Remove`, `RemoveSuffix`, `RemoveSuffix`, `ReplaceAt`, `ReplaceAt`, `ReverseString`, `RxFindAll`, `RxFindAll`, `RxFindAll`, `RxFindAll`, `RxIsMatch`, `RxMatch`, `RxMatch`, `RxMatch`, `RxReplace`, `RxReplace`, `RxReplace`, `RxReplace`, `RxSplit`, `SplitAnySE`, `SplitAnySE`, `SplitAnySE`, `SplitAnySE`, `SplitSE`, `SplitSE`, `SplitSE`, `SplitSE`, `Starts`, `Starts`, `Starts`, `ToInt`, `ToInt`, `ToInt`, `ToInt`, `ToInt`, `ToInt`, `ToInt`, `ToInt`, `ToInt`, `ToInt`, `ToNumber`, `ToNumber`, `ToNumber`, `ToNumber`, `ToNumber`, `ToNumber`, `ToNumber`, `ToStringUTF8`, `ToStringUTF8`, `ToStringUTF8`, `ToUTF8`, `ToUTF8`, `ToUTF8`, `Trim`, `TrimEnd`, `TrimStart`, `Unescape`, `Unescape`, `Upper`, `Upper`