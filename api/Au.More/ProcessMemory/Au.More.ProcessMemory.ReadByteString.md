# Method `Au.More.ProcessMemory.ReadByteString`

Copies a `byte` string from that process (memory address `Au.More.ProcessMemory.Mem`) to this process. In that process the string must be array of bytes (not Unicode UTF-16).

```
public string ReadByteString(int length, int offsetBytes = 0, bool findLength = false, Encoding enc = null)
```

##### Parameters

- *length*  (`int`):
    Number bytes to copy, not including the terminating `'\0'`. In that process a character is 1 or more bytes (depending on encoding). In this process will be 2 bytes (normal C# string).
- *offsetBytes*  (`int`):
    Offset in `Au.More.ProcessMemory.Mem`.
- *findLength*  (`bool`):
    Find string length by searching for `'\0'` character in *length* range.
- *enc*  (`Encoding`):
    Encoding for converting `byte` string to `char` string. If `null`, uses `System.Text.Encoding.Default` (UTF-8).

##### Returns

`string`

The copied string, or `null` if failed.