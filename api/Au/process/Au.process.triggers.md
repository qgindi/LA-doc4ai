# Method `Au.process.triggers`

Provides process started/ended triggers in `foreach` loop. See examples.

```csharp
public static IEnumerable<ProcessTriggerInfo> triggers(bool? started = null, string processName = null, bool ofThisSession = false, int period = 100)
```

##### Parameters

- *started*  (`bool?`):
  Trigger events: `true` - started, `false` - ended, `null` (default) - both.
- *processName*  (`string`):
  Process executable file name, like `"abc.exe"`.
  String format:[wildcard expression](🔗).
  `null` matches all.
- *ofThisSession*  (`bool`):
  Watch processes only of this user session.
- *period*  (`int`):
  The period in milliseconds of retrieving the list of processes for detecting new and ended processes. Default 100, min 10, max 1000.
  Smaller = smaller average delay and less missing triggers (when process lifetime is very short) but more CPU usage.

##### Returns

`IEnumerable<Au.Types.ProcessTriggerInfo>`

An object that retrieves process trigger info (started/ended, name, id, session id) when used with `foreach`.
If need more process properties, your code can call`Au.process` class functions with the process id.

##### Exceptions

- `ArgumentException`:
  Invalid wildcard expression (`"**options "` or regular expression).

#### Examples

```csharp
//all started and ended processes
foreach (var v in process.triggers()) {
	print.it(v);
}

//started mspaint.exe processes in current user session
foreach (var v in process.triggers(started: true, "mspaint.exe", ofThisSession: true)) {
	print.it(v);
}
```