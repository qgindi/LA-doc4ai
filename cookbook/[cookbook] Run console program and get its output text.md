# Run console program and get its output text

Function `Au.run.console` executes a console program in invisible mode and gets text that would be displayed in the console window.

Print the output text. Also this example uses command line arguments.

```
string v = "example";
int r1 = run.console(@"C:\Test\console1.exe", $@"/a ""{v}"" /etc");
```

Let my callback function receive output text lines in real time.

```
run.console(s => print.it(s), @"C:\Test\console2.exe"); //print it

run.console(s => { //or do whatever with it
	if (s.Starts("Error")) throw new Exception(s);
}, @"C:\Test\console2.exe");
```

Get the output text when the program exits. This example also uses the *encoding* parameter.

```
run.console(out var text, @"C:\Test\console3.exe", encoding: Console.OutputEncoding);
print.it(text);
```

If the output contains garbage text, need to specify encoding, like in the above example. Most console programs use `Encoding.UTF8`, `Encoding.Unicode` or `Console.OutputEncoding`. If not specified, `run.console` uses `Encoding.UTF8`.

See also: `Au.consoleProcess`.