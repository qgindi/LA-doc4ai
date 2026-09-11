# Script testing and debugging

When creating, testing and debugging scripts and other code, often you want to see what code parts are executed, what are values of variables there, etc. For it can be used `Au.print.it`. You can insert it temporarily, and later delete or disable the code line.

```csharp
print.it("Script started");
Test(5);
print.it("Script ended");

void Test(int i) {
	print.it("Test", i);
	//print.it("disabled");
}
```

To get the call stack, use `StackTrace`.

```csharp
F1();
void F1() { F2(); }
void F2() { F3(); }
void F3() { print.it(new StackTrace(0, true)); }
```

See also classes in namespace `System.Diagnostics` and its child namespaces.

```csharp
script.setup(debug: true);
// ...
Debug.Assert(false);
```

Also you can use a [debugger](🔗). It can execute script in step mode (one statement at a time), and in each step show variables, call stack, etc.