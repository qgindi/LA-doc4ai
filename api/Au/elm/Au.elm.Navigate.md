# Method `Au.elm.Navigate`

Gets an adjacent or related UI element - next, child, parent, etc.

```
public elm Navigate(string navig, double waitS = 0)
```

##### Parameters

- *navig*  (`string`):

    String consisting of one or more navigation direction strings separated by space, like `"parent next child4 first"`.

    - `"next"` - next sibling UI element in the same parent UI element.
    - `"previous"` - previous sibling UI element in the same parent UI element.
    - `"first"` - first child UI element.
    - `"last"` - last child UI element.
    - `"parent"` - parent (container) UI element.
    - `"child"` - child UI element by 1-based index. Example: `"child3"` (3-th child). Negative index means from end, for example -1 is the last child.
    - `"#N"` - custom. More info in Remarks.
    - Some elements also support `"up"`, `"down"`, `"left"`, `"right"`.
- *waitS*  (`double`):
    Wait for the wanted UI element max this number of seconds. Default 0 (don't wait). If negative, waits forever.

##### Returns

`Au.elm`

`null` if not found.

##### Exceptions

- `ArgumentException`:
    Invalid *navig* string.

#### Remarks

Can be 2 letters, like `"pr"` for `"previous"`. A string like `"next3"` or `"next,3"` is the same as `"next next next"`. Except for `"child"`. Use string like `"#1000"` to specify a custom *navDir* value to pass to `IAccessible.accNavigate`.

For `"child"` the function calls API `AccessibleChildren`. For `"parent"` the function calls `IAccessible.get_accParent`. Few UI elements don't support. Some UI elements return a different parent than in the tree of UI elements. For others the function calls `IAccessible.accNavigate`. Not all UI elements support it. Some UI elements skip invisible siblings. Instead you can use `"parent childN"` or `"childN"`.

#### Examples

```
a = e.Navigate("parent next ch3");
```