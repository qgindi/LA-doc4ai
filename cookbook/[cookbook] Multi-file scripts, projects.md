# Multi-file scripts, projects

A [script project](🔗) folder can contain one script and multiple class files that contain classes, structs, etc used in the script. Also you can place resource files there.

Script example:

```csharp
Class1.Function1("example");
```

Class file example:

```csharp
class Class1 {
	public static void Function1(string s) {
		print.it(s);
	}
}
```

Also in a script project you can split the [script class](🔗) into multiple files: one script and several [partial class](🔗) files.

Script example (note the `partial`):

```csharp
partial class Program {
	static void Main(string[] a) => new Program(a);
	Program(string[] args) {
		
		Function2("example");
		
	}
}
```

Partial class file example:

```csharp
partial class Program {
	void Function2(string s) {
		print.it(s);
	}
}
```

See also recipe [Shared classes](🔗).