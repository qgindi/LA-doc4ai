# File properties - `r` (button **Library**)

Add a .NET assembly reference. Meta comment `/*/ r File.dll; /*/`.

Don't need to add `Au.dll` and .NET runtime dlls.
 To remove this meta comment, edit the code in the code editor.
 If script role is `editorExtension`, may need to restart editor.

In code you can add some properties, like `/*/ r DllFile /property1|property2; /*/`:

- To not copy the dll to the output directory: `noCopy`
- To use `extern alias Abc;`: `alias=Abc`