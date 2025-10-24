# Struct `Au.Types.MRelease`

At the end of `using(...) { ... }` block releases mouse buttons pressed by the function that returned this variable. See example.

```
public struct MRelease : IDisposable
```

##### Examples

Drag and drop: start at x=8 y=8, move 20 pixels down, drop.

```
using(mouse.leftDown(w, 8, 8)) mouse.moveBy(0, 20); //the button is auto-released when the 'using' code block ends
```

### Methods

`Dispose`

### Operators

`implicit operator MRelease(MButton)`