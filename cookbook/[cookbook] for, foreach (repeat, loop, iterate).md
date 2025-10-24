# for, foreach (repeat, loop, iterate)

The [`for`](https://www.google.com/search?q=iteration+statements%2C+%22for%22%2C+C%23+reference) statement repeatedly executes statements.

```
for (int i = 0; i < 3; i++) { //increment i: 0, 1, 2
	print.it(i);
}
```

The above code declares variable *i* = 0. Then, while *i* is less than 3, executes statements in the `{ }` block and increments *i* (`i++`).

Several ways to insert `for` code quickly:

- Type text like `3t` (it means "repeat 3 times").
- Type `forl` and select `forLoopSnippet`.
- Click or select code, and use menu **Edit > Selection > Surround**.

```
for (int i = 3; --i >= 0; ) { //decrement i: 2, 1, 0
	print.it(i);
}

for (;;) { //repeat forever or until break/return/goto/throw
	500.ms(); //wait 500 ms
	print.it(1);
	if (keys.isCtrl) break; //exit the for block
	if (keys.isShift) continue; //skip remaining statements
	print.it(2);
}

for (int i = 0, j = 0; i < 5 && !keys.isShift; i++, j+=10) {
	print.it(i, j);
	500.ms();
}

//find space or tab in string
string s = "Abc def";
int k = 0;
for (; k < s.Length; k++) if (s[k] is ' ' or '\t') break;
print.it(k);
```

The `foreach` statement executes statements for each item in a collection (array, list, etc).

```
var a = new int[] { 3, 5, 10 }; //array
foreach (var v in a) {
	print.it(v);
}
```

The `while` statement is similar to `for`.

```
while (!keys.isCtrl) { //same as for (; !keys.isCtrl; )
	print.it("waiting for Ctrl");
	100.ms();
}
```