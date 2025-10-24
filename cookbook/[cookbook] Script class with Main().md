# Script class with Main()

The default script syntax is known as [C# top-level statements](https://www.google.com/search?q=C%23+top-level+statements). You can instead use the classic C# syntax with class `Program` and function `Main`. To insert code can be used menu **Edit > Generate > Add function Main**.

```
class Program {
	static void Main(string[] a) => new Program(a);
	Program(string[] args) {
		script.setup(trayIcon: true, sleepExit: true);
		
		print.it("script code");
		_field1 = 1;
		Function1();
		
	}
	
	int _field1; //this is a field, not a local variable
	void Function1() { } //this is a class function, not a local function
	
}
```

Why to use such code? Because the default syntax has some limitations. The classic syntax allows to:

- Add fields (class-level variables) and class-level functions to the main class.
- Add class/method-level modifiers and attributes, for example `partial`, `unsafe`, `[MTAThread]`.
- Split the main class into partial files. See recipe [Multi-file scripts](Multi-file%20scripts%2C%20projects.html).
- Avoid [intellisense](https://www.google.com/search?q=intellisense) failures that sometimes happen when typing code not in a { } block.

You can remove code `=> new Program(a); Program(string[] args)`. It just makes writing code a bit easier, because then don't need to use static functions and static fields. It creates a class instance, and the script code is executed in the constructor.