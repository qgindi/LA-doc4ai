# Method `Au.clipboardData.getHtml`

## Overload 1

Gets HTML text from the clipboard. Uses clipboard format `Au.Types.ClipFormats.Html` (`"HTML Format"`).

```
public static string getHtml()
```

##### Returns

`string`

`null` if there is no data of this format or if failed to parse it.

##### Exceptions

- `Au.Types.AuException`:
    Failed to open clipboard (after 10 s of wait/retry).

* * *

## Overload 2

Gets HTML text from the clipboard. Uses clipboard format `Au.Types.ClipFormats.Html` (`"HTML Format"`).

```
public static string getHtml(out int fragmentStart, out int fragmentLength, out string sourceURL)
```

##### Parameters

- *fragmentStart*  (`int`):
    Fragment start index in the returned string.
- *fragmentLength*  (`int`):
    Fragment length.
- *sourceURL*  (`string`):
    Source URL, or `null` if unavailable.

##### Returns

`string`

`null` if there is no data of this format or if failed to parse it.

##### Exceptions

- `Au.Types.AuException`:
    Failed to open clipboard (after 10 s of wait/retry).