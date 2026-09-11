# Comments, disabled code

Comments are used to explain code or temporarily disable code. It can be any text, it isn't executed.

```csharp
//This is a line comment.
print.it(1); //another comment

/*
This
is a block comment.
*/
print.it(1 /*another comment*/);

//print.it("disabled");
//print.it("code");
```

Two quick ways to convert code to comments and back:

1. Right-click the gray margin at the left. Select several lines if need.
2. Select or click the code, and click toolbar button **Toggle comment**.

[XML documentation comments](🔗) start with `///`.

LibreAutomate-specific comments:

```csharp
/*/ metacomments created by the Properties dialog /*/

//.
print.it("folded code");
print.it("like #region/#endregion");
//..
```

Another way to disable code - [#if, #endif, #else, #elif and #define](🔗).

```csharp
#if true
print.it(1);
// ...
#else
print.it(2);
// ...
#endif
```