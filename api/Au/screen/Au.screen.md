# Struct `Au.screen`

Represents a screen device. Gets its rectangle etc.

```
public struct screen : IEquatable<screen>
```

##### Remarks

A computer can have one or more screens (aka display devices, monitors). One of them is the *primary* screen; its top-left coordinate is 0 0. To show or find a window or some object in a particular screen, need to identify the screen somehow. At Windows API level each screen has a unique integer identifier, known as screen handle or `HMONITOR`. But it is a random variable value and therefore cannot be specified directly in script etc. Instead can be used screen index or some object on that screen (window, point, rectangle).

A `screen` variable can contain either a screen handle or a callback function that returns a screen handle. If empty, most functions interpret it as the primary screen.

To create `screen` variables use static functions (like `screen.index(1)` or `screen.primary`) or constructors (like `new screen(()=>screen.index(1))`) or `Au.screen.at`. Then call non-static functions to get screen properties.

A screen handle cannot be reliably used for a long time. Screen handles may change when changing the configuration of multiple screens. Consider a "lazy" variable, ie with callback function `Au.screen.LazyFunc`. Then, whenever a function needs a screen handle, it calls the callback function which returns a `screen` with fresh handle.

### Constructors

`screen(Func<screen>)`, `screen(nint)`

### Properties

`Dpi`, `Handle`, `Info`, `IsAlive`, `IsEmpty`, `LazyFunc`, `Now`, `Rect`, `ScreenIndex`, `WorkArea`, `all`, `ofActiveWindow`, `ofMouse`, `primary`, `virtualScreen`

### Methods

`Equals`, `Equals`, `GetHashCode`, `GetRect`, `ToString`, `index`, `isInAnyScreen`, `isInAnyScreen`, `isInAnyScreen`, `of`, `of`, `of`, `of`, `of`, `of`, `of`, `of`

### Operators

`operator ==(screen, screen)`, `operator !=(screen, screen)`