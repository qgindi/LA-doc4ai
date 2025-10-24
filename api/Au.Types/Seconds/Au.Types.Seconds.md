# Struct `Au.Types.Seconds`

Used with wait functions. Contains a wait timeout in seconds, and possibly wait options.

```
public struct Seconds
```

##### Remarks

Many wait functions of this library internally use `Au.More.WaitLoop`. They have a timeout parameter of `Seconds` type which allows to pass timeout and more options to `WaitLoop` in single parameter. You can pass a `Seconds` variable, like `new(3, period: 5)`. If don't need options etc, you can pass just timeout, like `3` or `0.5`.

Other wait functions have a timeout parameter of `Seconds` type but instead of `WaitLoop` use various hooks, events, Windows wait API, etc. They support only these `Seconds` properties: `Time`, `Cancel`, maybe `DoEvents`. Some always work like with `DoEvents` `true`.

More info: [Wait timeout](../articles/Wait%20timeout.html).

##### Examples

```
var w = wnd.find(new Seconds(3) { Period = 5, MaxPeriod = 50 }, "Name");
```

```
var to = new Seconds(0) { MaxPeriod = 50 };
wait.until(to, () => keys.isCtrl );
wait.until(to with { Time = 30 }, () => keys.isCtrl );
```

### Constructors

`Seconds(double)`

### Properties

`Cancel`, `DoEvents`, `MaxPeriod`, `Period`, `Time`

### Operators

`implicit operator Seconds(double)`