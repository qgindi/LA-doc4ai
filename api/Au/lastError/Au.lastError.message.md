# Property `Au.lastError.message`

Gets the text message of the Windows API last error code of this thread.

```
public static string message { get; }
```

##### Property Value

`string`

`null` if the code is 0.

#### Remarks

The string always ends with `"."`.