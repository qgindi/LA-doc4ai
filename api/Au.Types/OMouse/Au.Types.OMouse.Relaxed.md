# Property `Au.Types.OMouse.Relaxed`

Make some functions less strict (throw less exceptions etc). Default: `false`.

```
public bool Relaxed { get; set; }
```

##### Property Value

`bool`

#### Remarks

This option is used by these functions:

- `Au.mouse.move`, `Au.mouse.click` and other functions that move the cursor (mouse pointer):
`false` - throw exception if cannot move the cursor to the specified x y. For example if the x y is not in screen.
`true` - try to move anyway. Don't throw exception, regardless of the final cursor position (which probably will be at a screen edge).
- `Au.mouse.move`, `Au.mouse.click` and other functions that move the cursor (mouse pointer):
`false` - before moving the cursor, wait while a mouse button is pressed by the user or another thread. It prevents an unintended drag-drop.
`true` - do not wait.
- `Au.mouse.click` and other functions that click or press a mouse button using window coordinates:
`false` - don't allow to click in another window. If need, activate the specified window (or its top-level parent). If that does not help, throw exception. However if the window is a control, allow x y anywhere in its top-level parent window.
`true` - allow to click in another window. Don't activate the window and don't throw exception.

#### Examples

```
opt.mouse.Relaxed = true;
```