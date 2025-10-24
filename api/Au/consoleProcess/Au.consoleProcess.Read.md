# Method `Au.consoleProcess.Read`

Waits and reads next full or partial line.

```
public bool Read(out string s)
```

##### Parameters

- *s*  (`string`):
    Receives the text. It does not contain newline characters (`'\r'`, `'\n'`).

##### Returns

`bool`

`false` if there is no more text to read because the console process ended or is ending.

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Remarks

Waits for new text from console, reads it into an internal buffer, and then returns it one line at a time.

Sets `Au.consoleProcess.IsLine` = `true` if the line text in the buffer is terminated with newline characters. Else sets `IsLine` = `false`.

When `IsLine` is `false`, *s* text can be either a prompt (incomplete line that asks for user input) or an incomplete line/prompt text (the remainder will be retrieved later). Your script should somehow distinguish it. If it's a known prompt, let it call `Au.consoleProcess.Write`. Else call `Au.consoleProcess.Wait`. See example.

It's impossible to automatically distinguish a prompt from a partial line or partial prompt. The console program can write line text in parts, possibly with delays in between. Or it can write a prompt text and wait for user input. Also this function may receive line text in parts because of limited buffer size etc.

#### Examples

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