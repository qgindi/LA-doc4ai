# Method `Au.More.ProcessMemory.WriteByteString`

Copies a string from this process to that process (memory address `Au.More.ProcessMemory.Mem`). In that process writes the string as `'\0'`-terminated `byte` string.

```
public bool WriteByteString(string s, int offsetBytes = 0, Encoding enc = null)
```

##### Parameters

- *s*  (`string`):
    A string in this process. Normal C# string (UTF-16).
- *offsetBytes*  (`int`):
    Offset in `Au.More.ProcessMemory.Mem`.
- *enc*  (`Encoding`):
    Encoding for converting `char` string to `byte` string. If `null`, uses `System.Text.Encoding.Default` (UTF-8).

##### Returns

`bool`

`false` if failed.