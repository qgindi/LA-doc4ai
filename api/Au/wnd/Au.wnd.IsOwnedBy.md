# Method `Au.wnd.IsOwnedBy`

Returns `true` if this window is directly or indirectly owned by window *w*.

```
public bool IsOwnedBy(wnd w, int level)
```

##### Parameters

- *w*  (`Au.wnd`)
- *level*  (`int`):

    Return `true` if:

    - 0 - *w* is direct owner. See `Au.wnd.getwnd.Owner`.
    - 1 - *w* is direct or indirect owner (eg owner's owner).
    - 2 - *w* is direct or indirect owner, or this is a menu-like window that looks like owned by *w* (same thread, topmost, etc).

##### Returns

`bool`

#### Remarks

Many popup menus and similar temporary windows don't have an owner window. Instead they have topmost style. If *level* is 2, this function tries to detect this case. In most cases it works, but not always (depends on styles).