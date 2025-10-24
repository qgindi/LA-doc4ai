# C# introduction

[C#](https://learn.microsoft.com/en-us/dotnet/csharp/) is used to create script code in this program. It is one of the [most popular](https://www.google.com/search?q=programming+language+popularity) programming languages.

You don't need to learn C# to start creating automation scripts. Use the input recorder and other tools in the **Code** menu. But with some C# knowledge you can do much more.

This script displays string `"example"` in the program's **Output** panel. It calls function `it` of class `print`.

```
print.it("example");
```

This script contains 2 statements. The `//green text` is comments.

```
var s = "Some text."; //create variable s
dialog.show("Example", s); //show message box
```

Example with statements `if`, `return` (exit) and operator `!` (NOT).

```
if (!dialog.showOkCancel("Example", "Continue?")) {
	print.it("Cancel");
	return;
}
print.it("OK, let's continue.");
```

Use the `for` statement to execute code more than once.

```
for (int i = 0; i < 3; i++) {
	print.it(i);
}
```

Another way to execute code more than once - user-defined functions.

```
//call function Example 2 times
Example("one", 1);
Example("two",2);

//this is the function
void Example(string s, int i) {
	print.it(s.Upper() + " " + i);
}
```

In the above examples you also can see:

- The blue words are [C# keywords](https://www.google.com/search?q=C%23+keywords).
- Other words are [identifiers](https://www.google.com/search?q=C%23+identifiers) (names of types, functions, variables, etc).
- Keywords and identifiers are case-sensitive.
- Every statement ends with `;` (semicolon). Unless it starts a block of code enclosed in `{ }`.
- Function arguments are enclosed in `( )` and separated with `,` (comma).
- Blocks of code are enclosed in `{ }`.

C# does not care about the type and amount of whitespace (spaces, tabs, newlines) between statements, arguments, etc. Example:

```
Example("one",1);Example("two",
							2);
```