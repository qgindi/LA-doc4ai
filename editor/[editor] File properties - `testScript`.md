# File properties - `testScript`

A script to run when you click the **Run** button.

This property is for testing class files with role `classFile` or `classLibrary`. Such files cannot be executed directly.

The test script can contain meta comment `/*/ c this file.cs; /*/` that adds this file to the compilation, or `/*/ pr this file.cs; /*/` that adds the output dll file as a reference assembly. An easy way to add this property correctly is to try to run this file and click a link that is then printed in error text in the output.

The value can be:

- Path in the workspace. Examples: `\Script5.cs`, `\Folder\Script5.cs`.
- Path relative to this file. Examples: `Folder\Script5.cs`, `.\Script5.cs`, `..\Folder\Script5.cs`.
- Filename. Error if multiple exist, unless single exists in the same folder.

This property is saved in `files.xml`, not in meta comments.