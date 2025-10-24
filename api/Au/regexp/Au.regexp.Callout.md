# Property `Au.regexp.Callout`

Sets callout callback function.

```
public Action<RXCalloutData> Callout { set; }
```

##### Property Value

`Action<Au.Types.RXCalloutData>`

Callback delegate (eg lambda) or `null`.

#### Remarks

Callouts can be used to:

- Track the matching progress.
- Get all instances of a group that can match multiple times.
- Evaluate and reject some matches or match parts.
- Etc. The callback function is called by `Au.regexp.IsMatch`, `Au.regexp.Match`, `Au.regexp.FindAll`, `Au.regexp.Replace`, `Au.regexp.Split` and similar functions, when they reach callout points in regular expression. To insert callout points use `(?C)`, `(?C1)`, `(?C2)`, `(?C'name')` etc or pass flag `AUTO_CALLOUT` to the constructor. More info in PCRE help topic [pcre2callout](https://www.pcre.org/current/doc/html/pcre2callout.html). See also: https://www.rexegg.com/pcre-callouts.html

#### Examples

Track the matching progress.

```
var s = "text <a href='url'>link</a> text";
var rx = @"(?C1)<a (?C2)href='.+?'>(?C3)[^<]*(?C4)</a>";
var x = new regexp(rx);
x.Callout = o => { print.it(o.callout_number, o.start_match, o.current_position, s[o.start_match..o.current_position], rx.Substring(o.pattern_position, o.next_item_length)); };
print.it(x.IsMatch(s));
```

Track the matching progress with flag `AUTO_CALLOUT`.

```
var s = "one 'two' three";
var rx = @"'(.+?)'";
var x = new regexp(rx, RXFlags.AUTO_CALLOUT);
x.Callout = o => print.it(o.current_position, o.pattern_position, rx.Substring(o.pattern_position, o.next_item_length));
print.it(x.IsMatch(s));
```

Get all instances of a group that can match multiple times.

```
var s = "BEGIN 111 2222 333 END";
var x = new regexp(@"^(\w+) (?:(\d+) (?C1))+(\w+)$");
var a = new List<string>();
x.Callout = o => a.Add(o.LastGroupValue);
if(!x.Match(s, out var m)) { print.it("no match"); return; }
print.it(m[1]);
print.it(a); //all numbers. m[2] contains only the last number.
print.it(m[3]);
```

Evaluate and reject some matches or match parts. This code rejects matches longer than 5.

```
var s = "one 123-5 two 12-456 three 1-34 four";
var x = new regexp(@"\b\d+-\d+\b(?C1)");
x.Callout = o => { int len = o.current_position - o.start_match; /*print.it(len);*/ if(len > 5) o.Result = 1; };
print.it(x.FindAll(s, 0));
```