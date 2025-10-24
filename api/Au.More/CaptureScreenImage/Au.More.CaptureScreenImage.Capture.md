# Method `Au.More.CaptureScreenImage.Capture`

## Overload 1

Captures image from window client area into memory stored in this variable.

```
public bool Capture(wnd w, RECT? r = null, CIFlags flags = CIFlags.WindowDC)
```

##### Parameters

- *w*  (`Au.wnd`):
    Window or control.
- *r*  (`Au.Types.RECT?`):
    Rectangle in *w* client area coordinates. If `null`, uses `w.ClientRect`.
- *flags*  (`Au.Types.CIFlags`)

##### Returns

`bool`

`false` if *r* empty or not in the client area and used flag `Relaxed` (else exception).

* * *

## Overload 2

Captures image from screen into memory stored in this variable.

```
public bool Capture(RECT r, bool relaxed = false)
```

##### Parameters

- *r*  (`Au.Types.RECT`)
- *relaxed*  (`bool`):
    If *r* empty, return `false` instead of exception.

##### Returns

`bool`

`false` if *r* empty and *relaxed* `true` (else exception).