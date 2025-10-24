# Property `Au.computer.tickCountWithoutSleep`

Gets the number of milliseconds elapsed since Windows startup, not including the time when the computer sleeps or hibernates. To get time with sleep, use `System.Environment.TickCount64`.

```
public static long tickCountWithoutSleep { get; }
```

##### Property Value

`long`

#### Remarks

Uses API `QueryUnbiasedInterruptTime`. Uses the low-resolution system timer. Its period usually is 15.25 ms. Independent of computer clock time changes.