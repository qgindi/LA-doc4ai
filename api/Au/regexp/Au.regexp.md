# Class `Au.regexp`

PCRE regular expression.

```
public class regexp
```

##### Remarks

PCRE is a regular expression library: https://www.pcre.org/. PCRE regular expression syntax: [full](https://www.pcre.org/current/doc/html/pcre2pattern.html), [short](https://www.pcre.org/current/doc/html/pcre2syntax.html). Some websites with tutorials and info: [rexegg](https://www.rexegg.com/), [regular-expressions.info](https://www.regular-expressions.info/).

This class is an alternative to the .NET `System.Text.RegularExpressions.Regex` class. The regular expression syntax is similar. PCRE has some features unavailable in .NET, and vice versa. In most cases PCRE is faster. You can use any of these classes. Functions of `Au.elm` class support only PCRE.

Terms used in this documentation and in names of functions and types:

- *regular expression* - regular expression string. Also known as *pattern*.
- *subject string* - the string in which to search for the regular expression. Also known as *input string*.
- *match* - the part (substring) of the subject string that matches the regular expression.
- *groups* - regular expression parts enclosed in `()`. Except non-capturing parts, like `(?:...)` and `(?options)`. Also known as *capturing group*, *capturing subpattern*. Often term *group* also is used for group matches.
- *group match* - the part (substring) of the subject string that matches the group. Also known as *captured substring*.

This library uses an unmanaged code dll `AuCpp.dll` that contains PCRE code. This class is a managed wrapper for it. The main PCRE API functions used by this class are [pcre2_compile and pcre2_match](https://www.pcre.org/current/doc/html/pcre2api.html). The `regexp` constructor calls `pcre2_compile` and stores the compiled code in the variable. Other `regexp` functions call `pcre2_match`. Compiling to native code (JIT) is not supported.

A `regexp` variable can be used by multiple threads simultaneously.

Also there are several `System.String` extension methods that use this class. The string variable is the subject string. These methods create and use cached `regexp` instances for speed. The `regexp` constructor does not use caching.

##### Examples

```
var s = "one two22, three333,four"; //subject string
var x = new regexp(@"\b(\w+?)(\d+)\b"); //regular expression

print.it("//IsMatch:");
print.it(x.IsMatch(s));

print.it("//Match:");
if(x.Match(s, out var m)) print.it(m.Value, m[1].Value, m[2].Value);

print.it("//FindAll with foreach:");
foreach(var v in x.FindAll(s)) print.it(v.Value, v[1].Value, v[2].Value);
print.it("//FindAll, get only strings of group 2:");
print.it(x.FindAll(s, 2));

print.it("//Replace:");
print.it(x.Replace(s, "'$2$1'"));
print.it("//Replace with callback:");
print.it(x.Replace(s, o => o.Value.Upper()));
print.it("//Replace with callback and ExpandReplacement:");
print.it(x.Replace(s, o => { if(o.Length > 5) return o.ExpandReplacement("'$2$1'"); else return o[1].Value; }));

print.it("//Split:");
print.it(new regexp(@" *, *").Split(s));
```

Examples with `System.String` extension methods.

```
var s = "one two22, three333,four"; //subject string
var rx = @"\b(\w+?)(\d+)\b"; //regular expression

print.it("//RxIsMatch:");
print.it(s.RxIsMatch(rx));

print.it("//RxMatch:");
if(s.RxMatch(rx, out var m)) print.it(m.Value, m[1].Value, m[2].Value);

print.it("//RxMatch, get only string:");
if(s.RxMatch(rx, 0, out var s0)) print.it(s0);
print.it("//RxMatch, get only string of group 1:");
if(s.RxMatch(rx, 1, out var s1)) print.it(s1);

print.it("//RxFindAll with foreach:");
foreach(var v in s.RxFindAll(rx)) print.it(v.Value, v[1].Value, v[2].Value);

print.it("//RxFindAll with foreach, get only strings:");
foreach(var v in s.RxFindAll(rx, 0)) print.it(v);
print.it("//RxFindAll with foreach, get only strings of group 2:");
foreach(var v in s.RxFindAll(rx, 2)) print.it(v);

print.it("//RxFindAll, get array:");
if(s.RxFindAll(rx, out var am)) foreach(var k in am) print.it(k.Value, k[1].Value, k[2].Value);

print.it("//RxFindAll, get array of strings:");
if(s.RxFindAll(rx, 0, out var av)) print.it(av);
print.it("//RxFindAll, get array of group 2 strings:");
if(s.RxFindAll(rx, 2, out var ag)) print.it(ag);

print.it("//RxReplace:");
print.it(s.RxReplace(rx, "'$2$1'"));

print.it("//RxReplace with callback:");
print.it(s.RxReplace(rx, o => o.Value.Upper()));
print.it("//RxReplace with callback and ExpandReplacement:");
print.it(s.RxReplace(rx, o => { if(o.Length > 5) return o.ExpandReplacement("'$2$1'"); else return o[1].Value; }));

print.it("//RxReplace, get replacement count:");
if(0 != s.RxReplace(rx, "'$2$1'", out var s2)) print.it(s2);

print.it("//RxReplace with callback, get replacement count:");
if(0 != s.RxReplace(rx, o => o.Value.Upper(), out var s3)) print.it(s3);

print.it("//RxSplit:");
print.it(s.RxSplit(@" *, *"));
```

##### Inheritance

`object` → `regexp`

### Constructors

`regexp(string, RXFlags)`

### Properties

`Callout`

### Methods

`FindAll`, `FindAll`, `FindAll`, `FindAll`, `FindAllG`, `FindAllG`, `GetGroupNumberOf`, `GetMaxGroupNumber`, `IsMatch`, `IsMatch`, `Match`, `Match`, `Match`, `Match`, `Match`, `Replace`, `Replace`, `Replace`, `Replace`, `Split`, `SplitG`, `addReplaceFunc`, `escapeQE`