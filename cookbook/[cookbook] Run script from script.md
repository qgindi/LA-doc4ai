# Run script from script

To start another script, use `Au.script.run`. To insert code, drag and drop the script, or use snippet `srScriptRunSnippet`.

```
script.run(@"\Folder\Script.cs");
```

Pass arguments.

```
script.run(@"Script123.cs", "argument 1", "argument 2");
```

The script can get arguments like this:

```
if (args.Length > 0) { //args is a special variable of type string[]
	foreach (var v in args) {
		print.it(v);
	}
}
```

If need to wait until the script ends, use `Au.script.runWait`.

```
script.runWait(@"\Folder\Script.cs");
```

Pass arguments and get results.

```
script.runWait(out var ret, @"\Folder\Script.cs", "arg");
```

Get results in real time, without waiting until the script process ends.

```
script.runWait(s => { print.it(s); }, @"\Folder\Script.cs");
```

To return results as strings, that script calls `Au.script.writeResult` one or more times.

```
script.writeResult("result 1");
script.writeResult("result 2");
```

Also the script can return an int value. Then function `script.runWait` in the caller script returns it.

```
return 2;
```

Restart this script.

```
if (!dialog.showYesNo("Restart")) return;
script.restart();
return;
```

Scripts don't have a "trigger" property, but you can use `script.run` in hotkey/autotext/mouse/window trigger actions.