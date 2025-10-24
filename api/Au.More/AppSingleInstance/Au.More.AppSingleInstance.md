# Class `Au.More.AppSingleInstance`

Implements "single instance process" feature.

```
public static class AppSingleInstance
```

##### Examples

```
/*/ role exeProgram; ifRunning run; /*/
if (script.testing) args = ["test", "args"];

if (AppSingleInstance.AlreadyRunning("unique-mutex-name", args)) {
	print.it("already running");
	return;
}

var b = new wpfBuilder("Window").WinSize(400);
b.R.AddOkCancel();
b.End();
AppSingleInstance.Notified += a => {
	print.it("AppSingleInstance.Notified", a);
	b.Window.Activate();
};
if (!b.ShowDialog()) return;
```

##### Inheritance

`object` → `AppSingleInstance`

### Methods

`AlreadyRunning`

### Events

`Notified`

### See Also

`Au.script.single`