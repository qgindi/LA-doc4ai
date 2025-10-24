# Method `Au.consoleProcess.ReadAllText`

## Overload 1

Reads all console output text until its process ends. Returns that text.

```
public string ReadAllText()
```

##### Returns

`string`

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Remarks

Does not parse lines. Does not normalize newline characters.

* * *

## Overload 2

Reads all console output text until its process ends. Calls callback function.

```
public void ReadAllText(Action<string> output)
```

##### Parameters

- *output*  (`Action<string>`):
    Called for each text chunk received from console.

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Remarks

Does not parse lines. Does not normalize newline characters.