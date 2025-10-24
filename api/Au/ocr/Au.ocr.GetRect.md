# Method `Au.ocr.GetRect`

Gets the rectangle of the found word.

```
public RECT GetRect(bool inScreen, int word = 0)
```

##### Parameters

- *inScreen*  (`bool`):
    Convert to screen coordinates. If `false`, it's in *area* coordinates (window client area, etc) without rectangle offset.
- *word*  (`int`):
    Word index offset from `Au.ocr.FoundWordIndex`.

##### Returns

`Au.Types.RECT`