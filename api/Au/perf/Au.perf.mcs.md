# Property `Au.perf.mcs`

Gets the number of microseconds elapsed since Windows startup. Uses the high-resolution system timer (API `QueryPerformanceCounter`).

```csharp
public static long mcs { get; }
```

##### Property Value

`long`

#### Remarks

This function is used to measure time differences with 1 microsecond precision, like `var t1=perf.mcs; ... var t2=perf.mcs; var diff=t2-t1;`.
Independent of computer clock time changes.
See also:[Acquiring high-resolution time stamps](🔗).

### See Also

`Au.perf`