# Struct `Au.More.WaitLoop`

Can be used to easily implement "wait for" functions with a timeout.

```
public struct WaitLoop
```

##### Remarks

See examples. The code works like most "wait for" functions of this library: throws exception when timed out, unless the timeout value is negative. Similar code is used by `Au.wait.until<T>` and many other "wait for" functions of this library.

##### Examples

```
public static bool WaitForMouseLeftButtonDown(Seconds timeout) {
	var x = new WaitLoop(timeout);
	for(; ; ) {
		if(mouse.isPressed(MButtons.Left)) return true;
		if(!x.Sleep()) return false;
	}
}
```

The same with `Au.wait.until<T>`.

```
static bool WaitForMouseLeftButtonDown2(Seconds timeout) {
	return wait.until(timeout, () => mouse.isPressed(MButtons.Left));
}
```

### Constructors

`WaitLoop(Seconds)`

### Properties

`Cancel`, `MaxPeriod`, `Period`, `TimeRemaining`

### Methods

`IsTimeout`, `Sleep`