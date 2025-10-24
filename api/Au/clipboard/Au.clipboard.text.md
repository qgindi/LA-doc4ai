# Property `Au.clipboard.text`

Gets or sets clipboard text.

```
public static string text { get; set; }
```

##### Exceptions

- `Au.Types.AuException`:
    Failed to open clipboard (after 10 s of wait/retry) or set clipboard data.
- `OutOfMemoryException`:
    The `set` function failed to allocate memory.

##### Property Value

`string`

`null` if there is no text.

#### Remarks

The `get` function calls `Au.clipboardData.getText`.

Gets/sets only data of text format. For other formats (files, HTML, image, etc) use `Au.clipboardData` class.