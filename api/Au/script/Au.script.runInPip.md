# Method `Au.script.runInPip`

Starts executing a script in child session running in picture-in-picture (PiP) window. Does not wait.

```
public static void runInPip(string script, params string[] args)
```

##### Parameters

- *script*  (`string`):
    Script name like `"Script5.cs"`, or path like `@"\Folder\Script5.cs"`.
- *args*  (`string[]`):
    Command line arguments. In the script it will be variable *args*. Should not contain `'\0'` characters.

##### Exceptions

- `FileNotFoundException`:
    Script file not found.
- `Au.Types.AuException`:
    Script editor not running (in this session). No exception if cannot run the script in PiP session.