# Method `Au.More.ScriptEditor.TestCurrentFileInProject`

If a specified class file is currently active in editor, calls a callback function (which can be or call a function in that file) and returns true.

```
public static bool TestCurrentFileInProject(params (string file, Action action)[] files)
```

##### Parameters

- *files*  (`(string file, Action action)[]`):

    List of tuples `(string file, Action action)`:

    - `file` - a class file from current project; must be filename without ".cs" and path.
    - `action` - a callback function to call if that file is the active file in editor.

##### Returns

`bool`

#### Remarks

A script project folder can contain one script file at the top, and any number of class files. When you click **Run**, the code execution starts from the script, even if a class file is currently active in editor. But sometimes you may want to execute just a function in the current class file, and skip script code. The example shows how to do it easily.

#### Examples

Code at/near the start of the script file of a script project.

```
if (script.testing && ScriptEditor.TestCurrentFileInProject(("TaskA", TaskA.Func1), ("TaskB", () => TaskB.Func1(5)))) return;
```

File TaskA.cs.

```
static class TaskA {
	public static void Func1() {
		dialog.show(null, "TaskA");
	}
}
```

File TaskB.cs.

```
static class TaskB {
	public static void Func1(int x) {
		dialog.show(null, $"TaskB, x={x}");
	}
}
```