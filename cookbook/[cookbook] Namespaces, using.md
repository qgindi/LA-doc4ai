# Namespaces, using

Namespaces are containers for types (classes etc) and other namespaces. Like folders. Types in libraries (.NET etc) always are in namespaces. It allows to avoid conflicts with types in other libraries.

In a script these types can be used in two ways:

- At the start of the script (but after `/*/ ... /*/`) add [`using`](https://www.google.com/search?q=using+directive%2C+C%23+reference) directives with names of namespaces you want to use.
- Prepend `Namespace.` to the type name.

```
using System;
using System.Drawing;

Console.WriteLine("test"); //Console is a type from namespace System
Color c; //Color is a type from namespace System.Drawing

System.Windows.Window w; //Window is a type from namespace System.Windows
```

In scripts don't need `using` directives for `global using` namespaces that are in file `global.cs`.

In scripts don't need to create namespaces, but here is an example.

```
namespace Ns1 {
public class Class1 {
	public static void Func1() {  }
	public static void Func2() {  }
}

public class Class2 {
	public static void Func1() {  }
	public static void Func2() {  }
}
}

namespace Ns2 {
public class Class1 {
	public static void Func1() {  }
	public static void Func2() {  }
}

public class Class3 {
	public static void Func1() {  }
	public static void Func2() {  }
}
}
```

In the examples there are two classes named `Class1`. But that's OK, because they are in different namespaces. If in a script you want to use both these classes, prepend the namespace name to the class name.

```
Ns1.Class1.Func1();
Ns2.Class1.Func1();
```