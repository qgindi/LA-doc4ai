# Method `Au.clipboardData.contains`

## Overload 1

Returns `true` if the clipboard contains data of the specified format.

```
public static bool contains(int format)
```

##### Parameters

- *format*  (`int`):
    Clipboard format id. See `Au.Types.ClipFormats`.

##### Returns

`bool`

#### Remarks

Calls API `IsClipboardFormatAvailable`.

* * *

## Overload 2

Returns the first of the specified formats that is in the clipboard. Returns 0 if the clipboard is empty. Returns -1 if the clipboard contains data but not in any of the specified formats.

```
public static int contains(params int[] formats)
```

##### Parameters

- *formats*  (`int[]`):
    Clipboard format ids. See `Au.Types.ClipFormats`.

##### Returns

`int`

#### Remarks

Calls API `GetPriorityClipboardFormat`.