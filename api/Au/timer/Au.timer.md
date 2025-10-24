# Class `Au.timer`

Timer that calls callback function in same thread, which must have a message loop.

```
public class timer
```

##### Remarks

Uses API `SetTimer` and `WM_TIMER`. Works only in threads that have a message loop which retrieves/dispatches posted messages. For example threads with windows (except console). Timer action delegates are protected from GC.

##### Examples

This example sets 3 timers.

```
timer.after(500, _ => print.it("after 500 ms"));
timer.every(1000, _ => print.it("every 1000 ms"));
var t3 = new timer(_ => print.it("after 3000 ms")); t3.After(3000); //the same as timer.after
dialog.show("timer"); //shows a dialog window and waits until closed. The dialog retrieves/dispatches messages in its message loop.
```

##### Inheritance

`object` → `timer`

### Constructors

`timer(Action<timer>)`

### Properties

`IsRunning`, `Tag`

### Methods

`After`, `Every`, `Now`, `Stop`, `after`, `every`