# Multi-file scripts, projects

A [script project](/editor/Class%20files,%20projects.html) folder can contain one script and multiple class files that contain classes, structs, etc used in the script. Also you can place resource files there.

Script example:

```
Class1.Function1("example");
```

Class file example:

```
class Class1 {
	public static void Function1(string s) {
		print.it(s);
	}
}
```

Also in a script project you can split the [script class](Script%20class%20with%20Main%28%29.html) into multiple files: one script and several [partial class](https://www.google.com/search?q=C%23+partial+class) files.

Script example (note the `partial`):

```
partial class Program {
	static void Main(string[] a) => new Program(a);
	Program(string[] args) {
		
		Function2("example");
		
	}
}
```

Partial class file example:

```
partial class Program {
	void Function2(string s) {
		print.it(s);
	}
}
```

See also recipe [Shared classes](Shared%20classes%20and%20functions%2C%20libraries.html).