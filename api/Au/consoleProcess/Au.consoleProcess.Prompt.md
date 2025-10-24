# Method `Au.consoleProcess.Prompt`

Waits for next prompt (incomplete line that asks for user input). Reads the prompt and all lines before it. Then can write input text and `"\n"`.

```
public List<string> Prompt(string prompt, string input = null)
```

##### Parameters

- *prompt*  (`string`):
    Prompt text. Format: [wildcard expression](../articles/Wildcard%20expression.html).
- *input*  (`string`):
    Input text. If `""`, writes just `"\n"`. If `null`, does not write.

##### Returns

`List<string>`

List of lines before the prompt. The last item is the prompt.

##### Exceptions

- `Au.Types.AuException`:
    Next prompt text does not match *prompt* (after waiting 5 s for full prompt). Or the console process ended. Or failed to write *input*.

#### Examples

```
using var c = new consoleProcess("example.exe");
c.Prompt("User: ", "A");
c.Prompt("Password: ", "B");
while (c.Read(out var s)) print.it(s);
```

```
var a = c.Prompt("User:");
print.it(a);
c.Write(a.Any(o => o.Contains("keyword")) ? "A" : "B");
```

```
using var c = new consoleProcess("cmd.exe");
var prompt = @"C:\*>";
c.Prompt(prompt, "example.exa");
foreach (var s in c.Prompt(prompt).SkipLast(1)) print.it(s);
c.Write("exit");
```