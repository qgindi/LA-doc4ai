# Class `Au.timer2`

Timer that calls callback function in other thread (thread pool) and can be used in any thread.

```
public class timer2
```

##### Remarks

Uses `System.Threading.Timer`. Unlike `Au.timer`, the thread that sets the timer does not have to retrieve/dispatch messages. The callback function is called in a random thread of the thread pool, therefore its code is not thread-safe (may need to lock etc). The actual minimal time interval/period is 10-20 ms, because the system timer period usually is 15.25 ms. Timer action delegates are protected from GC.

##### Examples

This example sets 3 timers.

```
timer2.after(500, _ => print.it("after 500 ms"));
timer2.every(1000, _ => print.it("every 1000 ms"));
var t3 = new timer2(_ => print.it("after 3000 ms")); t3.After(3000); //the same as timer2.after
5.s();
```

##### Inheritance

`object` → `timer2`

### Constructors

`timer2(Action<timer2>)`

### Properties

`Tag`

### Methods

`After`, `Every`, `Stop`, `after`, `every`