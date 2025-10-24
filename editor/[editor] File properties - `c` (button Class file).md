# File properties - `c` (button **Class file**)

Add a C# code file that contains some classes/functions used by this file. Meta comment `/*/ c File.cs; /*/`.

The compiler will compile all code files and create single assembly.

The file must be in this workspace. Import files if need (eg drag-drop). Can be a link.
 If folder, will compile all its descendant class files.
 The value can be:

- Path in the workspace. Examples: `\Class5.cs`, `\Folder\Class5.cs`.
- Path relative to this file. Examples: `Folder\Class5.cs`, `.\Class5.cs`, `..\Folder\Class5.cs`.
- Filename. Error if multiple exist, unless single exists in the same folder.

Don't use this meta comment to add class files that are in the same project folder. They are added automatically.

To remove this meta comment, edit the code.