# File properties - `file` (button **Other file**)

Make a file available at run time. Meta comment `/*/ file File; /*/`.

It can be any file, for example an unmanaged dll.

The compiler behavior depends on the role of the main file of the compilation:

- `exeProgram` - copy the file to the output folder. Or subfolder: `/*/ file file.dll /sub; /*/`.
- `miniProgram` or `editorExtension` - store the dll path in the assembly in order to find it at run time.
- `classLibrary` - the above actions are used when compiling scripts that use it as a project reference. The compiler does not copy these files to the output folder of the library.

The file must be in this workspace. Import files if need (eg drag-drop). Can be a link.
 The value can be:

- Path in the workspace. Examples: `\File.png`, `\Folder\File.png`.
- Path relative to this file. Examples: `Folder\File.png`, `.\File.png`, `..\Folder\File.png`.
- Filename. Error if multiple exist, unless single exists in the same folder.

If folder, will include all its descendant files. Will copy them into folders like in the workspace. If a folder name ends with `-`, will copy its contents only (will not create the folder).

If an `exeProgram` script uses unmanaged dll files, consider placing them in subfolders named `64`, `64\ARM` and `32`. Then at run time will be loaded the dll for that platform.

To remove this meta comment, edit the code.