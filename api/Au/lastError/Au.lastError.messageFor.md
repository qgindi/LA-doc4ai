# Method `Au.lastError.messageFor`

Gets the text message of a Windows API error code.

```
public static string messageFor(int errorCode)
```

##### Parameters

- *errorCode*  (`int`)

##### Returns

`string`

`null` if *errorCode* is 0.

#### Remarks

The string always ends with `"."`.