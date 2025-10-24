# Property `Au.script.name`

Gets the script name, like `"Script123"`.

```
public static string name { get; }
```

##### Property Value

`string`

#### Remarks

If role `miniProgram` (default), returns the script file name without extension. Else returns `System.AppDomain.FriendlyName`, like `"MainAssemblyName"`.