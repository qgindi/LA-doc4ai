# Method `Au.perf.cpu`

Executes some code in loop for the specified amount of time. It should make CPU to run at full speed.

```
public static void cpu(int timeMilliseconds = 200)
```

##### Parameters

- *timeMilliseconds*  (`int`):
    How long to speed up CPU, milliseconds. The minimal required time probably is about 100 ms, but depends on CPU.

#### Remarks

Code speed measurements often are misleading because of variable CPU speed. Most CPU don't run at full speed when not actively used.

You can make CPU speed constant in **Control Panel > Power Options > ... Advanced > Processor power management > Minimum or maximum power state**. There are programs that show current CPU speed. For example HWMonitor.