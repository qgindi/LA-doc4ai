# Property `Au.perf.ms`

Gets the number of milliseconds elapsed since Windows startup. Uses the high-resolution system timer (API `QueryPerformanceCounter`).

```
public static long ms { get; }
```

##### Property Value

`long`

#### Remarks

This function is used to measure time differences with 1 ms precision, like `var t1=perf.ms; ... var t2=perf.ms; var diff=t2-t1;`. The return value equals `Au.perf.mcs`/1000 but is slightly different than of `System.Environment.TickCount64` and most Windows API. Never compare times returned by different functions. Independent of computer clock time changes.