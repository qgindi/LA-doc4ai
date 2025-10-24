# Method `Au.elm.GetProperties`

Gets multiple properties.

```
public bool GetProperties(string props, out EProperties result)
```

##### Parameters

- *props*  (`string`):

    String that specifies properties to get, for example `"nv"` for name and value.

    - `R` - `Au.elm.Role`.
    - `n` - `Au.elm.Name`.
    - `v` - `Au.elm.Value`.
    - `d` - `Au.elm.Description`.
    - `h` - `Au.elm.Help`.
    - `a` - `Au.elm.DefaultAction`.
    - `k` - `Au.elm.KeyboardShortcut`.
    - `u` - `Au.elm.UiaId`.
    - `U` - `Au.elm.UiaCN`.
    - `s` - `Au.elm.State`.
    - `r` - `Au.elm.GetRect` with *raw* `true`.
    - `D` - `Au.elm.Rect` or `Au.elm.GetRect` with *raw* `false`. Don't use with `r`.
    - `w` - `Au.elm.WndContainer`.
    - `o` - `Au.elm.Html` outer.
    - `i` - `Au.elm.Html` inner.
    - `@` - `Au.elm.HtmlAttributes`.
- *result*  (`Au.Types.EProperties`):
    Receives results.

##### Returns

`bool`

`false` if failed, for example when the UI element's window is closed. Supports `Au.lastError`.

##### Exceptions

- `ArgumentException`:
    Unknown property character.

#### Remarks

The returned variable contains values of properties specified in *props*. When a property is empty or failed to get, the member variable is `""`, empty dictionary or default value of that type; never `null`.

Normally this function is faster than calling multiple property functions, because it makes single remote procedure call. But not if this UI element was found with flag `Au.Types.EFFlags.NotInProc` etc.