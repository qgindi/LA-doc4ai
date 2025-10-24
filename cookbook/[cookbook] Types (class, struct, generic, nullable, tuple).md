# Types (class, struct, generic, nullable, tuple)

In scripts we use [types](https://www.google.com/search?q=C%23+types) to create variables and to call functions.

```
string s = "text"; //variable s of type string
int k = 5; //variable k of type int
dialog.showInfo(s, k.ToString()); //call function showInfo which is defined in type dialog. Also call function ToString which is defined in type int.
```

`int`, `string` and some other types are built into the C# language; more info in recipe [Variables](Variables%2C%20fields%2C%20built-in%20types.html). Many other types are defined in .NET and other libraries, and `dialog` is an example. More examples:

```
DateTime dt = DateTime.Now; //variable dt of type DateTime. Also call function Now which is defined in type DateTime.
RECT r = new RECT(1, 2, 3, 4); //variable r of type RECT. Also call a constructor function defined in type RECT.
print.it(dt, r.left); //call function it which is defined in type print. Pass dt and r field left which is defined in type RECT.
```

There are 5 kinds of types:

- [class](https://www.google.com/search?q=C%23+class). Also known as *reference type*. Can contain data fields (variables, constants), functions (methods, properties, etc), events and inner types.
- [struct](https://www.google.com/search?q=C%23+struct). Also known as *value type*. Same as class, but variables are stored differently: the value is directly in the variable. A class variable is a reference (*pointer*) to its value that is stored separately, and the value isn't copied when copying the variable.
- [enum](https://www.google.com/search?q=C%23+enum). Defines several integer constants, and nothing else.
- [delegate](https://www.google.com/search?q=C%23+delegate). Defines a function type (parameters, etc).
- [interface](https://www.google.com/search?q=C%23+interface). Defines multiple function types.

You can define new types, with functions etc inside. Example in recipe [Functions](Functions%20%28methods%2C%20properties%29.html).

Also C# supports arrays, [generic types](https://www.google.com/search?q=C%23+generic+types), [nullable value types](https://www.google.com/search?q=C%23+nullable+value+types), [tuples](https://www.google.com/search?q=C%23+value+tuple+types), [anonymous types](https://www.google.com/search?q=C%23+anonymous+types) and [pointers](https://www.google.com/search?q=C%23+unsafe+pointers).

Generic types have names like `List<T>`. They can be used in several ways:

- Replace `T` with a type name, like `List<string>`. Examples in recipe [collections](Collections%20-%20array%2C%20List%2C%20Stack%2C%20Queue.html).
- If a parameter is of type `T`, can be used argument of any supported type.
- If an `out` parameter is of type `T`, argument code can be like `out string s`.

If a value-type variable is declared like `int? i`, you can assign it `null`, which could mean "no value". Often used for optional parameters.

```
void Func1(bool? b = null) {
	if (b == null) print.it("null");
	else if (b == true) print.it("true");
	else print.it(b.Value);
}
```

Variables of reference types always can have value `null`. If a function parameter or return type is like `string?`, it is just a hint that the function supports `null`.

Tuples contain several fields (variables) of possibly different types. Often used to returns multiple values from a function, like in the [Functions](Functions%20%28methods%2C%20properties%29.html) recipe.

```
(int i, string s) t = (10, "text"); //create a tuple variable t
print.it(t.i, t.s);
```