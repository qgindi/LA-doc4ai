# Interface `Au.Types.ITBOwnerObject`

Used with `Au.toolbar.Show`.

```
public interface ITBOwnerObject
```

##### Remarks

Allows a toolbar to follow an object in the owner window, for example a UI element or image. Or to hide in certain conditions. Define a class that implements this interface. Create a variable of that class and pass it to `Au.toolbar.Show`. The interface functions are called every 250 ms, sometimes more frequently. Not called when the owner window is invisible or cloaked or minimized.

### Properties

`IsAlive`, `IsVisible`

### Methods

`GetRect`