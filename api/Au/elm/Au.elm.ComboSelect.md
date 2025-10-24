# Method `Au.elm.ComboSelect`

Finds and selects an item in the drop-down list of this combo box or drop-down button.

```
public elm ComboSelect(string item, string how = null, double waitS = 3)
```

##### Parameters

- *item*  (`string`):
    Item name (`Au.elm.Name`). String format: [wildcard expression](../articles/Wildcard%20expression.html).
- *how*  (`string`):

    Try this parameter if the function fails to select the item etc.

    In the string can be used these characters to specify how to select the item and close the drop-down list:

    - `i` - call `Au.elm.Invoke`.
    - `s` - call `Au.elm.Select`.
    - `c` - close the list with `Au.elm.Expand`.
    - `m` - call `Au.elm.MouseClick`; often can't be used because fails to get correct rectangle or to scroll.
    - `k` - call `Au.elm.Focus` and `Au.keys.send` (`Home`, `Down`, `Enter`).
    - space - nothing.

    If the string is `null` (default) or `""` or does not contain these characters, the function tries to detect and use what usually works for this UI element type, but it's impossible to detect always.

    Usually need just a single character (string like `"i"` or `"m"`). If there are more characters, the functions are called in the specified order.

    The string also can contain sleep times. For example `"300m"` will wait 300 ms and click; the first sleep will be between expanding and finding.

    If the string starts with `"~"`, the function does not expand the drop-down list (it should be already expanded).

    If the string isn't `null`/empty but does not contain characters `iscmk` (for example is `" "` or `"~ "` or `"200 "`), the function does not select/close. For example these codes do the same: `e.ComboSelect("Red", "i");` and `e.ComboSelect("Red", " ").Invoke();`.
- *waitS*  (`double`):
    Seconds to wait for expanded state (if not 0) and for the item. Can be negative to avoid timeout exceptions.

##### Returns

`Au.elm`

The item.

##### Exceptions

- `ArgumentException`:
    Error in *item* string (wildex options or regex) or *how*.
- `Au.Types.NotFoundException`:
    Item not found.
- `Exception`:
    Exceptions of used functions.

#### Remarks

The function at first calls `Au.elm.Expand` to show the drop-down list, unless *how* starts with `"~"`. Then finds the item by name, selects it and closes the drop-down list.