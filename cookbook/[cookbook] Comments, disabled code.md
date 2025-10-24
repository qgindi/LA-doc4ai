# Comments, disabled code

Comments are used to explain code or temporarily disable code. It can be any text, it isn't executed.

```
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

[XML documentation comments](https://www.google.com/search?q=C%23+XML+documentation+comments) start with `///`.

Comments specific to this program:

```
/*/ metacomments created by the Properties dialog /*/

//.
print.it("folded code");
print.it("like #region/#endregion");
//..
```

Another way to disable code - [#if, #endif, #else, #elif and #define](https://www.google.com/search?q=directive+%23if+%23else%2C+C%23+reference).

```
#if true
print.it(1);
// ...
#else
print.it(2);
// ...
#endif
```