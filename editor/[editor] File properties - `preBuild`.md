# File properties - `preBuild`

A script to run before compiling.

The script must have role `editorExtension`. It runs in the editor's main thread.
 To get compilation info: `var c = PrePostBuild.Info;`
 To specify command line arguments: `/*/ preBuild Script5.cs /arguments; /*/`
 To stop the compilation, let the script throw an exception.
 To create new preBuild/postBuild script: menu **File > New > More**.

The value can be:

- Path in the workspace. Examples: `\Script5.cs`, `\Folder\Script5.cs`.
- Path relative to this file. Examples: `Folder\Script5.cs`, `.\Script5.cs`, `..\Folder\Script5.cs`.
- Filename. Error if multiple exist, unless single exists in the same folder.