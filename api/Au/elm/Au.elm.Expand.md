# Method `Au.elm.Expand`

## Overload 1

Expands or collapse this expandable UI element (tree item, combo box, expander, dropdown button).

```
public void Expand(bool expand = true, string keys = null, double waitS = 1, bool ignoreState = false)
```

##### Parameters

- *expand*  (`bool`):
    `true` to expand, `false` to collapse.
- *keys*  (`string`):
    If not `null`, makes this element focused and presses these keys. See `Au.keys.send`. If `""`, uses keys commonly used for that UI element type, for example `Right`/`Left` for `TREEITEM`, `Alt+Down` for `COMBOBOX`. If `null`, uses `Au.elm.Invoke` or similar functions, which often are available only if the element was found with flag `UIA`; if unavailable or fails, works like with *keys* `""`.
- *waitS*  (`double`):
    If not 0, waits for new expanded/collapsed state max this number of seconds; on timeout throws exception, unless negative.
- *ignoreState*  (`bool`):
    Ignore initial `EXPANDED`/`COLLAPSED` state and always perform the expand/collapse action. Can be useful when `Au.elm.State` `EXPANDED`/`COLLAPSED` is incorrect. To ignore final state, use negative *waitS* instead, for example -0.001.

##### Exceptions

- `Exception`:
    Exceptions of `Au.elm.SendKeys`.
- `TimeoutException`:
    The state didn't change in *waitS* seconds (if > 0).

#### Remarks

Does nothing if the UI element already has the requested expanded/collapsed state.

Works with UI elements that have `Au.elm.State` `EXPANDED` when expanded and `COLLAPSED` when collapsed. Also with UI elements that have state `CHECKED` or `PRESSED` when expanded and don't have this state when collapsed.

* * *

## Overload 2

Expands or collapse this expandable UI element (tree item, combo box, expander, dropdown button).

```
public void Expand(bool expand, Action<elm> action, double waitS = 1, bool ignoreState = false)
```

##### Parameters

- *expand*  (`bool`):
    `true` to expand, `false` to collapse.
- *action*  (`Action<Au.elm>`):
    Callback function that should expand or collapse this UI element. Its parameter is this variable.
- *waitS*  (`double`):
    If not 0, waits for new expanded/collapsed state max this number of seconds; on timeout throws exception, unless negative.
- *ignoreState*  (`bool`):
    Ignore initial `EXPANDED`/`COLLAPSED` state and always perform the expand/collapse action. Can be useful when `Au.elm.State` `EXPANDED`/`COLLAPSED` is incorrect. To ignore final state, use negative *waitS* instead, for example -0.001.

##### Exceptions

- `Exception`:
    Exceptions of the callback function.
- `TimeoutException`:
    The state didn't change in *waitS* seconds (if > 0).

#### Remarks

Does nothing if the UI element already has the requested expanded/collapsed state.

Works with UI elements that have `Au.elm.State` `EXPANDED` when expanded and `COLLAPSED` when collapsed. Also with UI elements that have state `CHECKED` or `PRESSED` when expanded and don't have this state when collapsed.

* * *

## Overload 3

Expands multiple treeview control items using a path string.

```
public elm Expand(Strings path, string keys = null, double waitS = 3, bool notLast = false)
```

##### Parameters

- *path*  (`Au.Types.Strings`):
    String or array consisting of names (`Au.elm.Name`) of `TREEITEM` elements, like `"One|Two|Three"` or `["One", "Two", "Three"]`. Name string format: [wildcard expression](../articles/Wildcard%20expression.html).
- *keys*  (`string`):
    `null` or keys to use to expand each element specified in *path*. See `Au.elm.Expand(bool, string, double, bool)`.
- *waitS*  (`double`):
    If not 0, after expanding each element waits for expanded state max this number of seconds; on timeout throws exception, unless negative. Also waits for each element this number of seconds; always exception if not found.
- *notLast*  (`bool`):
    Find but don't expand the last element specified in *path*. For example if it's not a folder, and therefore can't expand it, but you need to find it (this function returns it).

##### Returns

`Au.elm`

`Au.elm` of the last element specified in *path*.

##### Exceptions

- `ArgumentException`:
    *path* contains an invalid wildcard expression (`"**options "` or regular expression).
- `Au.Types.NotFoundException`:
    Failed to find an element specified in *path*.
- `Au.Types.AuException`:
    Failed.
- `TimeoutException`:
    The state didn't change in *waitS* seconds (if > 0).
- `NotSupportedException`:
    The treeview control type is not supported when this is a 32-bit process running on 64-bit OS (unlikely).
- `Exception`:
    Exceptions of `Au.elm.SendKeys`.

#### Remarks

This element can be a `TREE` or `TREEITEM`. If it is a collapsed `TREEITEM`, expands it. Then finds and expands elements specified in *path*.

Does not work if all `TREEITEM` elements in the `TREE` control are its direct children, unless it's the standard Windows treeview control.

* * *

## Overload 4

Expands multiple treeview control items using a path string.

```
public elm Expand(Strings path, Action<elm> action, double waitS = 3, bool notLast = false)
```

##### Parameters

- *path*  (`Au.Types.Strings`):
    String or array consisting of names (`Au.elm.Name`) of `TREEITEM` elements, like `"One|Two|Three"` or `["One", "Two", "Three"]`. Name string format: [wildcard expression](../articles/Wildcard%20expression.html).
- *action*  (`Action<Au.elm>`):
    Callback function that should expand UI elements.
- *waitS*  (`double`):
    If not 0, after expanding each element waits for expanded state max this number of seconds; on timeout throws exception, unless negative. Also waits for each element this number of seconds; always exception if not found.
- *notLast*  (`bool`):
    Find but don't expand the last element specified in *path*. For example if it's not a folder, and therefore can't expand it, but you need to find it (this function returns it).

##### Returns

`Au.elm`

`Au.elm` of the last element specified in *path*.

##### Exceptions

- `Exception`:
    Exceptions of the callback function.
- `ArgumentException`:
    *path* contains an invalid wildcard expression (`"**options "` or regular expression).
- `Au.Types.NotFoundException`:
    Failed to find an element specified in *path*.
- `Au.Types.AuException`:
    Failed.
- `TimeoutException`:
    The state didn't change in *waitS* seconds (if > 0).
- `NotSupportedException`:
    The treeview control type is not supported when this is a 32-bit process running on 64-bit OS (unlikely).