# File properties - `role`

The purpose of this C# code file. What kind of assembly to create and how to execute.

- `miniProgram` - execute in a separate host process started from editor.
- `exeProgram` - create/execute exe file, which can run on any computer, without editor installed.
- `editorExtension` - execute in the editor's UI thread. Rarely used. Incorrect code can kill editor.
- `classLibrary` - create dll file, which can be used in C# scripts and other .NET-based programs.
- `classFile` - don't create/execute. The C# code file can be compiled together with other C# code files in the project or using meta comment `c`. Inherits meta comments of the main file of the compilation.

Default role for scripts is `miniProgram`; cannot be the last two. Default for class files is `classFile`; can be any.

See also: [Scripts](Scripts.html), [Class files](Class%20files%2C%20projects.html), [Shared classes and functions, libraries](/cookbook/Shared classes and functions, libraries.html)