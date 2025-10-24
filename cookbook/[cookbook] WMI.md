# WMI

Use NuGet package System.Management. See also [System.Management namespace](https://www.google.com/search?q=System.Management+namespace).

```
/*/ nuget -\System.Management; /*/
using System.Management;
```

Create process.

```
var pr = new ManagementClass("Win32_Process");
pr.InvokeMethod("Create", new[] { "Notepad.exe" });
```

Get properties of all processes.

```
print.clear();
var scope = new ManagementScope(); scope.Connect();
var query = new ObjectQuery("SELECT * FROM Win32_Process");
var searcher = new ManagementObjectSearcher(scope, query);
foreach (var m in searcher.Get()) {
	print.it($"{m["Name"],-30}  {m["CommandLine"]}");
}
```

Watch process start events. Note: this is just an example of WMI events; if need real triggers, use [process triggers](Process%20triggers%20%28start%2C%20end%29.html).

```
using var watcher = new ManagementEventWatcher("SELECT * FROM __InstanceCreationEvent WITHIN 1 WHERE TargetInstance isa \"Win32_Process\"");
watcher.Options.Timeout = TimeSpan.FromSeconds(30);
using var osd = osdText.showTransparentText("Open 2 applications to trigger events", -1);
for (int i = 0; i < 2; i++) {
	var e = watcher.WaitForNextEvent();
	var v = (ManagementBaseObject)e["TargetInstance"];
	print.it(v["Name"], v["CommandLine"]);
}
```