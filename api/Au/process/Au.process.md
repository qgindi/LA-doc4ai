# Class `Au.process`

Process functions. Find, enumerate, get basic info, terminate, triggers, etc. Also includes properties and events of current process and thread.

```
public static class process
```

##### Inheritance

`object` → `process`

### Properties

`thisExeName`, `thisExePath`, `thisProcessCultureIsInvariant`, `thisProcessHandle`, `thisProcessId`, `thisProcessSessionId`, `thisThreadHandle`, `thisThreadId`

### Methods

`allProcesses`, `exists`, `getCommandLine`, `getDescription`, `getName`, `getProcessId`, `getProcessIds`, `getSessionId`, `getTimes`, `getVersionInfo`, `is32Bit`, `is32Bit`, `processIdFromHandle`, `suspend`, `suspend`, `terminate`, `terminate`, `thisProcessExitInvoke`, `thisThreadHasMessageLoop`, `thisThreadHasMessageLoop`, `triggers`, `waitForExit`

### Events

`thisProcessExit`

### See Also

`Au.run`

`Au.script`

`System.Diagnostics.Process`