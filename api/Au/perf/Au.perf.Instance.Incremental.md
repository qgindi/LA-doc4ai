# Property `Au.perf.Instance.Incremental`

See `Au.perf.incremental`.

```
public bool Incremental { get; set; }
```

##### Property Value

`bool`

#### Examples

```
var p1 = new perf.Instance { Incremental = true };
for(int i = 0; i < 5; i++) {
	Thread.Sleep(100); //not included in the measurement
	p1.First();
	Thread.Sleep(30); //will make sum ~150000
	p1.Next();
	Thread.Sleep(10); //will make sum ~50000
	p1.Next();
	Thread.Sleep(100); //not included in the measurement
}
p1.Write(); //speed:  154317  51060  (205377)
p1.Incremental = false;
```