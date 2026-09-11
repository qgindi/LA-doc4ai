# Errors, exceptions, try-catch-finally, throw

A script with errors can't run. Errors must be fixed.

```csharp
print.it(1) //error, no semicolon
print.it(u); //error, u does not exist
```

Exceptions occur when something fails at run time. Then the script ends or jumps to a `catch` part of the nearest `try-catch` statement that embraces that code. [More info](🔗).

```csharp
print.it(1);
try {
	var w = wnd.find(0, "* - Notepadd");
	print.it(2);
}
catch {
	print.it("exception");
	return; //remove this, and the script will continue at print.it(3);
	//throw; //add this instead of return, and the script will end like without try/catch
	//throw new InvalidOperationException("message"); //or throw another exception
}
print.it(3);
```

Can get exception info.

```csharp
try { run.it("notepad11.exe"); }
catch (Exception e) { print.it(e); }
print.it("continue");
```

Can differently handle exceptions of different types. Can use `when`.

```csharp
string text = null;
try { text = File.ReadAllText(@"D:\file45678"); }
catch (FileNotFoundException) { } //continue
catch (Exception e) when (e is not ArgumentException) { //handle all other exceptions except ArgumentException
	print.it(e.ToStringWithoutStack());
	return;
}
print.it(text ?? "file not found");
```

Can use `try-finally` and `try-catch-finally`. [More info](🔗). The `finally` code runs when the `try` code is leaved in whatever way (finished, exception, `return`, `goto`, etc).

```csharp
print.it(1);
try {
	run.it("notepad22.exe");
	print.it(2);
	if (keys.isCapsLock) return;
}
//catch { print.it("exception"); } //optional. Try to uncomment this and observe the difference.
finally { print.it("finally"); }
print.it(3);
```

Note: The `finally` code does not run if `Environment.Exit` or some other function terminates the process.

With disposable objects instead of `try-finally-Dispose` can be used the [`using`](🔗) statement.

To throw exceptions use the [`throw`](🔗) statement.

```csharp
Func1(1);
Func1(-1);

void Func1(int i) {
	if (i < 0) throw new ArgumentException("Can't be negative", nameof(i));
	if (keys.isCapsLock) throw new InvalidOperationException("CapsLock");
	print.it(i);
}
```

Two ways to insert `try` code quickly:

- Type `tryc` and select `trySnippet`.
- Click or select code, and use menu **Edit > Selection > Surround**.