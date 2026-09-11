# Method `Au.perf.write`

Formats a string from time values collected by calling `Au.perf.first` and `Au.perf.next`, and shows it in the output.
The string contains the number of microseconds of each code execution between calling`Au.perf.first` and each `Au.perf.next`.

```csharp
public static void write()
```

#### Examples

```csharp
perf.first(100);
CODE1;
perf.next();
CODE2;
perf.next();
perf.write(); //speed:  timeOfCODE1  timeOfCODE2  (totalTime)
```