# Property `Au.Types.RXMatch.Mark`

Gets the name of a found mark, or `null`.

```
public string Mark { get; }
```

##### Property Value

`string`

#### Remarks

Marks can be inserted in regular expression pattern like `(*MARK:name)` or `(*:name)`. After a full successful match, it is the last mark encountered on the matching path through the pattern. After a "no match" or a partial match, it is the last encountered mark. For example, consider this pattern: `"^(*MARK:A)((*MARK:B)a|b)c"`. When it matches `"bc"`, the mark is `A`. The `B` mark is "seen" in the first branch of the group, but it is not on the matching path. On the other hand, when this pattern fails to match `"bx"`, the mark is `B`.