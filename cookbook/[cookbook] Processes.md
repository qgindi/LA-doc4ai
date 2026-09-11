# Processes

A process is a running program. It can have visible windows or not. Also known as *task*. Use class `Au.process`.

Print names of all processes of this user session.

```csharp
print.clear();
var a = process.allProcesses(ofThisSession: true);
foreach (var v in a) {
	print.it(v.Name);
}
```

Terminate, suspend and resume all Notepad processes (end tasks).

```csharp
process.terminate("notepad.exe");
process.suspend(true, "notepad.exe");
process.suspend(false, "notepad.exe");
```

If process does not exist.

```csharp
if (!process.exists("notepad.exe")) {
	print.it("does not exist");
}
```

Wait for a Notepad process. See also [Process triggers](🔗).

```csharp
wait.until(0, () => process.exists("notepad.exe"));
```

Wait until there are no Notepad processes.

```csharp
wait.until(0, () => !process.exists("notepad.exe"));
```

Get window process id and terminate its process.

```csharp
var w1 = wnd.find(1, "*- Notepad", "Notepad");
int pid = w1.ProcessId;
process.terminate(pid);
```

Get window process name.

```csharp
var w2 = wnd.find(1, "*- Notepad", "Notepad");
var program = w2.ProgramName;
```

Get name and path of current process (the script process).

```csharp
print.it(process.thisExeName, process.thisExePath);
```

Get script name.

```csharp
print.it(script.name);
```

When need to get more process properties, use [Process](🔗) or [WMI](🔗).