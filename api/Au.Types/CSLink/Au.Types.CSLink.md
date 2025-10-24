# Enum `Au.Types.CSLink`

See `Au.filesystem.more.createSymbolicLink`

```
public enum CSLink
```

### Fields

| Name | Description |
| --- | --- |
| Directory | Symbolic link to directory. |
| File | Symbolic link to file. |
| Junction | (see section `details1` in Footnotes) |
| JunctionOrSymlink | Junction to local directory or symbolic link to network directory. |

## Footnotes

###### details1

Junction to directory.

Usually junctions work like symbolic links, but there are differences when creating them:

- Don't need admin privileges to create.
- Target must be full path. Fails if relative path.
- Target must be on this computer. Fails if on a network computer.
- Target must be directory. Fails if file.

Some programs interpret junctions differently. For example git adds the target directory.