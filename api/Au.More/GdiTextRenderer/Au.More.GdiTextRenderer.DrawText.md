# Method `Au.More.GdiTextRenderer.DrawText`

## Overload 1

Draws text at the current drawing position of the DC, and updates it.

```
public void DrawText(string s, int color = 0, Range? range = null, int? backColor = null)
```

##### Parameters

- *s*  (`string`)
- *color*  (`int`):
    Text color `0xBBGGRR`.
- *range*  (`Range?`)
- *backColor*  (`int?`):
    Background color `0xBBGGRR`. Transparent if `null`.

* * *

## Overload 2

Draws text at specified position. Does not use/update the current drawing position of the DC.

```
public void DrawText(string s, POINT p, int color = 0, Range? range = null, int? backColor = null)
```

##### Parameters

- *s*  (`string`)
- *p*  (`Au.Types.POINT`)
- *color*  (`int`):
    Text color `0xBBGGRR`.
- *range*  (`Range?`)
- *backColor*  (`int?`):
    Background color `0xBBGGRR`. Transparent if `null`.

* * *

## Overload 3

Draws text clipped in specified rectangle. Does not use/update the current drawing position of the DC.

```
public void DrawText(string s, in RECT r, int color = 0, Range? range = null, int? backColor = null)
```

##### Parameters

- *s*  (`string`)
- *r*  (`Au.Types.RECT`)
- *color*  (`int`):
    Text color `0xBBGGRR`.
- *range*  (`Range?`)
- *backColor*  (`int?`):
    Background color `0xBBGGRR`. Transparent if `null`.