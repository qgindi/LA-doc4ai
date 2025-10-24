# Class `Au.wildex`

Parses and compares [wildcard expression](../articles/Wildcard%20expression.html).

```
public class wildex
```

##### Remarks

Used in "find" functions. For example in `Au.wnd.find` to compare window name, class name and program. The "find" function creates a `wildex` instance (which parses the wildcard expression), then calls `Au.wildex.Match` for each item (eg window) to compare some its property text.

##### Examples

```
//This version does not support wildcard expressions.
Document Find1(string name, string date) {
	return Documents.Find(x => x.Name.Eqi(name) && x.Date.Eqi(date));
}

//This version supports wildcard expressions.
//null-string arguments are not compared.
Document Find2(string name, string date) {
	wildex n = name, d = date; //null if the string is null
	return Documents.Find(x => (n == null || n.Match(x.Name)) && (d == null || d.Match(x.Date)));
}

//Example of calling such function.
//Find item whose name is "example" (case-insensitive) and date starts with "2017-".
var item = x.Find2("example", "2017-*");
```

##### Inheritance

`object` → `wildex`

### Constructors

`wildex(string, bool, bool)`

### Properties

`IgnoreCase`, `MultiArray`, `Not`, `RegexNet`, `RegexPcre`, `Text`, `TextType`

### Methods

`Match`, `ToString`, `hasWildcardChars`

### Operators

`implicit operator wildex(string)`