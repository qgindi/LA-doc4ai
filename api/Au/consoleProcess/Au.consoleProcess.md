# Class `Au.consoleProcess`

Runs a console program in hidden mode. Gets its output text and can write input text.

```
public sealed class consoleProcess : IDisposable
```

##### Remarks

Must be disposed. In the example the `using` statement does it.

##### Examples

```
using var c = new consoleProcess(folders.Workspace + @"exe\console1\console1.exe");
//c.Encoding = Console.OutputEncoding;
while (c.Read(out var s)) {
	if (c.IsLine) {
		print.it($"<><c green><_>{s}</_><>");
	} else {
		if (s == "User: ") c.Write("A");
		else if (s == "Password: ") c.Write("B");
		//else if (c.Wait()) continue; //let next Read wait for more text and get old + new text. Use this if other prompts are not possible.
		else if (c.Wait(500)) continue; //wait for more text max 500 ms. If received, let next Read get old + new text.
		else if (dialog.showInput(out var s1, null, s)) c.Write(s1);
		//else print.it($"<><c blue><_>{s}</_><><nonl>");
		else throw new OperationCanceledException();
	}
}
if (c.ExitCode is int ec && ec != 0) throw new Exception($"Failed. Exit code: {ec}");
```

```
using var c = new consoleProcess("example.exe");
c.Prompt("User: ", "A");
c.Prompt("Password: ", "B");
while (c.Read(out var s)) print.it(s);
print.it(c.ExitCode);
```

##### Inheritance

`object` → `consoleProcess`

### Constructors

`consoleProcess(string, string, string)`

### Properties

`Encoding`, `Ended`, `ExitCode`, `InputEncoding`, `IsLine`, `TerminateFinally`

### Methods

`Dispose`, `Prompt`, `Read`, `ReadAllText`, `ReadAllText`, `ReadLine`, `TerminateNow`, `Wait`, `Write`

### See Also

`Au.run.console`