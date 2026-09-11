# Method `Au.consoleProcess.EndInput`

Closes the standard input stream (stdin), signaling end of input to the process.

```csharp
public void EndInput()
```

#### Remarks

Some console programs expect you to close stdin after writing all input data (see `Au.consoleProcess.Write`). This signals "end of file" (EOF).