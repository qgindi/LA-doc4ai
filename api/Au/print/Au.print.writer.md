# Property `Au.print.writer`

Gets or sets object that actually writes text when is called `Au.print.it`.

```
public static TextWriter writer { get; set; }
```

##### Property Value

`TextWriter`

#### Remarks

If you want to redirect or modify or just monitor output text, use code like in the example. It is known as "output redirection". Redirection is applied to whole process, not just this thread. Redirection affects `Au.print.it`, `Au.print.redirectConsoleOutput` and `Au.print.redirectDebugOutput`. It does not affect `Au.print.directly` and `Au.print.clear`. Don't call `Au.print.it` in method `WriteLine` of your writer class. It would call itself and create stack overflow. Call `Au.print.directly`, like in the example.

#### Examples

```
print.writer = new OutputWriterWithTime();

print.it("test");

class OutputWriterWithTime :TextWriter {
	public override void WriteLine(string value) { print.directly(DateTime.Now.ToString("T") + ".  " + value); }
	public override Encoding Encoding => Encoding.Unicode;
}
```