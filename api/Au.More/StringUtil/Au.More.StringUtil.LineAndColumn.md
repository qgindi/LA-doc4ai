# Method `Au.More.StringUtil.LineAndColumn`

Converts character index in string to line index and character index in that line.

```
public static void LineAndColumn(string s, int index, out int lineIndex, out int indexInLine)
```

##### Parameters

- *s*  (`string`)
- *index*  (`int`):
    Character index in string *s*.
- *lineIndex*  (`int`):
    Receives 0-based line index.
- *indexInLine*  (`int`):
    Receives 0-based character index in that line.

##### Exceptions

- `ArgumentOutOfRangeException`