# Property `Au.perf.mcs`

Gets the number of microseconds elapsed since Windows startup. Uses the high-resolution system timer (API `QueryPerformanceCounter`).

```
public static long mcs { get; }
```

##### Property Value

`long`

#### Remarks

This function is used to measure time differences with 1 microsecond precision, like `var t1=perf.mcs; ... var t2=perf.mcs; var diff=t2-t1;`. Independent of computer clock time changes. See also: [Acquiring high-resolution time stamps](https://www.google.com/search?q=Acquiring+high-resolution+time+stamps+site:microsoft.com).

### See Also

`Au.perf`