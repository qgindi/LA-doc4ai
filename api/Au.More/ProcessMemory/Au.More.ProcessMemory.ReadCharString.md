# Method `Au.More.ProcessMemory.ReadCharString`

Copies a `char` string from that process (memory address `Au.More.ProcessMemory.Mem`) to this process. In that process the string must be in Unicode UTF-16 format.

```
public string ReadCharString(int length, int offsetBytes = 0, bool findLength = false)
```

##### Parameters

- *length*  (`int`):
    Number of characters to copy, not including the terminating `'\0'`. In both processes a character is 2 bytes.
- *offsetBytes*  (`int`):
    Offset in `Au.More.ProcessMemory.Mem`.
- *findLength*  (`bool`):
    Find string length by searching for `'\0'` character in *length* range. If `false`, the returned string is of *length* length even if contains `'\0'` characters.

##### Returns

`string`

The copied string, or `null` if failed.