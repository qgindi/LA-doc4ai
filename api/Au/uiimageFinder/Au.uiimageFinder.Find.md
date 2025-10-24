# Method `Au.uiimageFinder.Find`

## Overload 1

Finds the first image displayed in the specified window or other area. See `Au.uiimage.find`.

```
public uiimage Find(IFArea area)
```

##### Parameters

- *area*  (`Au.Types.IFArea`):

    Where to search:

    - `Au.wnd` - window or control (its client area).
    - `Au.elm` - UI element.
    - `System.Drawing.Bitmap` - image.
    - `Au.Types.RECT` - a rectangle area in screen.
    - `Au.Types.IFArea` - can contain `Au.wnd`, `Au.elm` or `System.Drawing.Bitmap`. Also allows to specify a rectangle in it, which makes the area smaller and the function faster. Example: `new(w, (left, top, width, height))`.

##### Returns

`Au.uiimage`

If found, returns `Au.uiimageFinder.Result`, else `null`.

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid window handle.
- `ArgumentException`:
    An argument of this function or of constructor is invalid.
- `Au.Types.AuException`:
    Something failed.

#### Remarks

Functions `Find` and `Au.uiimageFinder.Exists` differ only in their return types.

* * *

## Overload 2

Finds the first image displayed in the specified window or other area. Can wait and throw `Au.Types.NotFoundException`.

```
public uiimage Find(IFArea area, Seconds wait)
```

##### Parameters

- *area*  (`Au.Types.IFArea`):

    Where to search:

    - `Au.wnd` - window or control (its client area).
    - `Au.elm` - UI element.
    - `System.Drawing.Bitmap` - image.
    - `Au.Types.RECT` - a rectangle area in screen.
    - `Au.Types.IFArea` - can contain `Au.wnd`, `Au.elm` or `System.Drawing.Bitmap`. Also allows to specify a rectangle in it, which makes the area smaller and the function faster. Example: `new(w, (left, top, width, height))`.
- *wait*  (`Au.Types.Seconds`):
    The wait timeout, seconds. If 0, does not wait. If negative, does not throw `Au.Types.NotFoundException`.

##### Returns

`Au.uiimage`

If found, returns `Au.uiimageFinder.Result`. Else throws exception or returns `null` (if *wait* negative).

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid window handle.
- `ArgumentException`:
    An argument of this function or of constructor is invalid.
- `Au.Types.AuException`:
    Something failed.
- `Au.Types.NotFoundException`

#### Remarks

Functions `Find` and `Au.uiimageFinder.Exists` differ only in their return types.