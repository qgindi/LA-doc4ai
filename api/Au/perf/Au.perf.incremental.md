# Property `Au.perf.incremental`

If `true`, times of each new `first next next...` measurement are added to previous measurement times. Finally you can call `Au.perf.write` or `Au.perf.toString` to get the sums. Usually used to measure code in loops. See example.

```
public static bool incremental { get; set; }
```

##### Property Value

`bool`

#### Examples

```
perf.incremental = true;
for(int i = 0; i < 5; i++) {
	Thread.Sleep(100); //not included in the measurement
	perf.first();
	Thread.Sleep(30); //will make sum ~150000
	perf.next();
	Thread.Sleep(10); //will make sum ~50000
	perf.next();
	Thread.Sleep(100); //not included in the measurement
}
perf.write(); //speed:  154317  51060  (205377)
perf.incremental = false;
```