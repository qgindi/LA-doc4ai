# Class `Au.Types.RXMatch`

Regular expression match info. Used with `Au.regexp` class functions and `System.String` extension methods like `Au.Types.ExtString.RxMatch`.

```
public class RXMatch
```

##### Remarks

Contains info about a regular expression match found in the subject string: index, length, substring, etc. Also contains an array of group matches, as `Au.Types.RXGroup`. Groups are regular expression parts enclosed in `()`, except `(?...)`. Group matches can be accessed like array elements. Group 0 is whole match. Group 1 is the first group. See examples.

##### Examples

```
var s = "ab cd-45-ef gh";
if(s.RxMatch(@"\b([a-z]+)-(\d+)\b", out RXMatch m))
	print.it(
		m.GroupCountPlusOne, //3 (whole match and 2 groups)
		m.Start, //3, same as m[0].Index
		m.Value, //"cd-45-ef", same as m[0].Value
		m[1].Start, //3
		m[1].Value, //"cd"
		m[2].Start, //6
		m[2].Value //"45"
		);
```

A group in the subject string may not exist even if whole match found. Then its `Au.Types.RXMatch.Exists` property is `false`, `Au.Types.RXMatch.Start` -1, `Au.Types.RXMatch.Length` 0, `Au.Types.RXMatch.Value` `null`.

```
var s = "ab cd--ef gh";
if(s.RxMatch(@"\b([a-z]+)-(\d+)?-([a-z]+)\b", out RXMatch m))
	print.it(
		m.GroupCountPlusOne, //4 (whole match and 3 groups)
		m[2].Exists, //false
		m[2].Start, //-1
		m[2].Length, //0
		m[2].Value //null
		);
```

##### Inheritance

`object` → `RXMatch`

### Properties

`End`, `Exists`, `GroupCountPlusOne`, `IsPartial`, `this[int]`, `this[string]`, `Length`, `Mark`, `Span`, `Start`, `StartNoK`, `Subject`, `Value`

### Methods

`ExpandReplacement`, `GroupNumberFromName`, `GroupNumberFromName`, `ToString`