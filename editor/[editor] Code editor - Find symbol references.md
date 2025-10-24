# Code editor - Find symbol references

The **Find references** command takes the symbol (class name, function name, variable, etc) at the current position and finds all places in current and related files where the symbol is used. Ignores matching words in comments, strings and `#if`-disabled code. Displays results in the **Found** panel. You can click a result line to go to that place. You can middle-click to close the file if it was opened from that results.

The **Find implementations** command is similar. If the symbol is an interface or class, finds types that implement or inherit it. If the symbol is an interface/abstract/virtual function, finds functions that implement or override it.

What is "related files":

- If current file is part of a @Project folder - all files of that project.
- Files used by current file/project through `/*/ c /*/`.
- If current file or project uses project references (`/*/ pr /*/`) and that project can use that symbol - all files of that projects.
- If the symbol definition file or project is used by other files or projects through `c` or `pr` - all that files/projects.
- If the symbol is defined in a dll or `global.cs`, does not search in entire workspace (it could be slow or gather many unwanted results), but searches in files/projects that use current file/project through `c`/`pr`.