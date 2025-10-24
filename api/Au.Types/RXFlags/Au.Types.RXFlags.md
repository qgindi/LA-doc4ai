# Enum `Au.Types.RXFlags`

Flags for `Au.regexp` constructor. Documented in PCRE help topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html).

```
[Flags]
public enum RXFlags : ulong
```

##### Remarks

Many options also can be specified in regular expression (RE):

- These can be anywhere in RE: `(?i)` `CASELESS`, `(?m)` `MULTILINE`, `(?s)` `DOTALL`, `(?n)` `NO_AUTO_CAPTURE`, `(?x)` `EXTENDED`, `(?xx)` `EXTENDED_MORE`, `(?J)` `DUPNAMES`, `(?U)` `UNGREEDY`. Can be multiple, like `(?ms)`. Can be unset, like `(?-i)`. RE `"\Qtext\E"` is like RE `"text"` with flag `LITERAL`.
- Instead of `ANCHORED` can be used `\G` at the start of RE. Or `^`, except in multiline mode.
- Instead of `ENDANCHORED` can be used `\z` at the end of RE. Or `$`, except in multiline mode.
- Flag UTF is implicitly added if RE contains non-ASCII characters and there is no flag `NEVER_UTF`.
- These must be at the very start and are named like flags: `(*UTF)`, `(*UCP)`, `(*NOTEMPTY)`, `(*NOTEMPTY_ATSTART)`, `(*NO_AUTO_POSSESS)`, `(*NO_DOTSTAR_ANCHOR)`, `(*NO_START_OPT)`.
- More info in [PCRE syntax reference](https://www.pcre.org/current/doc/html/pcre2pattern.html).

Some of `RXFlags` flags also exist in `Au.Types.RXMatchFlags`. You can set them either when calling `Au.regexp` constructor or when calling `Au.regexp` functions that have parameter *more*. You can use different flags for each function call with the same `Au.regexp` variable.

### Fields

| Name | Description |
| --- | --- |
| ALLOW_EMPTY_CLASS | Allow empty classes |
| ALT_BSUX | Alternative handling of `\u`, `\U`, and `\x` |
| ALT_CIRCUMFLEX | Alternative handling of `^` in multiline mode |
| ALT_EXTENDED_CLASS | Alternative extended character class syntax |
| ALT_VERBNAMES | Process backslashes in verb names |
| ANCHORED | Match only at the first position |
| AUTO_CALLOUT | Compile automatic callouts |
| CASELESS | Do caseless matching |
| DOLLAR_ENDONLY | `$` not to match newline at end |
| DOTALL | `.` matches anything including newlines |
| DUPNAMES | Allow duplicate names for subpatterns |
| ENDANCHORED | Pattern can match only at end of subject |
| EXTENDED | Ignore white space and `#` comments |
| EXTENDED_MORE |  |
| EXTRA_ASCII_BSD | `\d` remains ASCII in UCP mode |
| EXTRA_ASCII_BSS | `\s` remains ASCII in UCP mode |
| EXTRA_ASCII_BSW | `\w` remains ASCII in UCP mode |
| EXTRA_ASCII_DIGIT | `[:digit:]` and `[:xdigit:]` POSIX classes remain ASCII in UCP mode |
| EXTRA_ASCII_POSIX | POSIX classes remain ASCII in UCP mode |
| EXTRA_CASELESS_RESTRICT | Disable mixed ASCII/non-ASCII case folding |
| EXTRA_MATCH_LINE | Pattern matches whole lines |
| EXTRA_MATCH_WORD | Pattern matches "words" |
| EXTRA_NEVER_CALLOUT | Disallow callouts in pattern |
| EXTRA_TURKISH_CASING | Use Turkish I case folding |
| FIRSTLINE | Force matching to be before newline |
| LITERAL | Pattern characters are all literal |
| MATCH_INVALID_UTF | Enable support for matching invalid UTF |
| MATCH_UNSET_BACKREF | Match unset backreferences |
| MULTILINE | `^` and `$` match newlines within data |
| NEVER_BACKSLASH_C | Lock out the use of `\C` in patterns |
| NEVER_UCP | Lock out `UCP`, e.g. via `(*UCP)` |
| NEVER_UTF | Lock out `UTF`, e.g. via `(*UTF)` |
| NOTBOL | Subject string is not the beginning of a line |
| NOTEMPTY | An empty string is not a valid match |
| NOTEMPTY_ATSTART | An empty string at the start of the subject is not a valid match |
| NOTEOL | Subject string is not the end of a line |
| NO_AUTO_CAPTURE | Disable numbered capturing paren-theses (named ones available) |
| NO_AUTO_POSSESS | Disable auto-possessification |
| NO_DOTSTAR_ANCHOR | Disable automatic anchoring for `.*` |
| NO_START_OPTIMIZE | Disable match-time start optimizations |
| NO_UTF_CHECK | Do not check the pattern for UTF validity |
| PARTIAL_HARD | Allow partial hard match. See `Au.Types.RXMatch.IsPartial`. |
| PARTIAL_SOFT | Allow partial soft match. See `Au.Types.RXMatch.IsPartial`. |
| UCP | Use Unicode properties for `\d`, `\w`, etc |
| UNGREEDY | Invert greediness of quantifiers |
| UTF | Fully support Unicode text (case-insensitivity etc). More info in PCRE documentation topic [pcre2unicode](https://www.pcre.org/current/doc/html/pcre2unicode.html). This flag is implicitly added if regular expression contains non-ASCII characters and there is no flag `NEVER_UTF`. |