# Method `Au.Types.ExtString.FindWord`

Finds whole word. Returns its 0-based index, or -1 if not found.

```
public static int FindWord(this string t, string s, Range? range = null, bool ignoreCase = false, string otherWordChars = null, Func<char, bool> isWordChar = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *s*  (`string`):
    Substring to find.
- *range*  (`Range?`):
    The search range.
- *ignoreCase*  (`bool`):
    Case-insensitive.
- *otherWordChars*  (`string`):
    Additional word characters. For example `"_"`.
- *isWordChar*  (`Func<char, bool>`):
    Function that returns `true` for word characters. If `null`, uses `char.IsLetterOrDigit`.

##### Returns

`int`

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *range*.

#### Remarks

If *s* starts with a word character, finds substring that is not preceded by a word character. If *s* ends with a word character, finds substring that is not followed by a word character. Word characters are those for which *isWordChar* or `char.IsLetterOrDigit` returns `true` plus those specified in *otherWordChars*. Uses ordinal comparison (does not depend on current culture/locale). For Unicode surrogates (2-`char` characters) calls `char.IsLetterOrDigit` and ignores *isWordChar* and *otherWordChars*.