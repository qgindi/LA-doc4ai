# Method `Au.More.ProcessMemory.WriteCharString`

Copies a string from this process to that process (memory address `Au.More.ProcessMemory.Mem`). In that process writes the string as `'\0'`-terminated `char` string (UTF-16).

```
public bool WriteCharString(string s, int offsetBytes = 0)
```

##### Parameters

- *s*  (`string`):
    A string in this process.
- *offsetBytes*  (`int`):
    Offset in `Au.More.ProcessMemory.Mem`.

##### Returns

`bool`

`false` if failed.

#### Remarks

In that process is used `(s.Length+1)*2` bytes of memory (+1 for the `'\0'`, `*` 2 because UTF-16 character size is 2 bytes).