# Code editor | other

## Bracket completion

When you type `(`, `[`, `{`, `<`, `"` or `'`, editor adds the closing `)`, `]`, `}`, `>`, `"` or `'`. Then, while the text cursor is before the added `)` etc, typing another `)` or `Tab` just leaves the enclosed area. Also then `Backspace` erases both characters.

## Auto indentation

On `Enter` editor adds new line with correct indentation.

## Parameter info

When you type a function name and `(`, editor shows a tooltip-like window with info about the function and current parameter. To show the window from anywhere in an argument list, press `Ctrl+Shift+Space`. You can select oveloads with arrow keys or the mouse.

## Quick info

Whenever the mouse dwells on a symbol etc in the editor, a tooltip displays some info about the symbol, including documented exceptions the function may throw.

## Error info

Errors are detected in editor, as well as when compiling the code. Code parts with errors have red squiggly underlines, warnings green. A tooltip shows error/warning description. Also can contain links to fix the error, for example add a missing `using namespace` or Windows API declaration.

## Go to symbol documentation

To show symbol documentation if available, press `F1` when the text cursor is in it. Or click the **more info** link in the autocompletion item info or parameter info window.

If the symbol is from the automation library, it opens the online documentation page in your web browser. If the symbol is from .NET runtime or other assembly or unmanaged code (`[DllImport]` or `[ComImport]`), it opens the Google search page.

## Go to script, file, URL

Click a file path string and press `F12` to select it in File Explorer. In the same way you can open folders, script files and web pages. It also works in meta comments, other comments and in code like `folders.System + @"notepad.exe"`. If the path etc does not start and end with `"`, at first select it.

## Find and replace text

Use the **Find** panel to find and replace text in editor. It marks all matches in editor with yellow. Also can find files by name and files containing text. Can replace text in multiple files.

## Outline of current file

The **Outline** panel shows functions and fields defined in current file. Also types, if there are multiple. And regions. Click to go to the definition.

## Navigate back/forward

The **Back** and **Forward** buttons work like in web browsers.

## Bookmarks

You can mark lines in code, and later go there. Use menu **Edit > Navigate**, panel **Bookmarks** and the markers margin.

Menu commands **Previous bookmark** and **Next bookmark** visit only active bookmarks. If there are no active bookmarks - only bookmarks in current document.

## Code coloring

Different kinds of code parts have different colors. Comments, strings, keywords, types, functions, etc.

## Text folding

You can hide and show code regions like in a tree view control: click the **[-]** or **[+]** in the left margin. Folding is available for functions, events, types, multiline comments, disabled code (`#if`), `#region` ... `#endregion`, `//.` ... `//..`, namespaces, local functions, lambda, initializer lists and strings.

`Ctrl`+click to show/hide descendant folds as well. `Shift`+click to show descendants. For more options right-click the folding margin.

## Separators between functions/types

Editor draws horizontal lines at the end of each function and type definition.

## Snippets

The autocompletion list also contains [snippets](🔗). For example the `outSnippet` inserts code `print.it();` when you type `out` and space or `Tab` or `Enter` or click it. Some snippets are in the **Surround** menu.

## Images in code

If a code line contains a string or comment with a file path, embedded image (screenshot, `"image:"`) or `"*icon"`, editor draws the image at the left. Also captures screenshots when recording etc. Embedded image data usually is hidden.

This feature can be enabled/disabled with the toolbar button.

## Format code

The **Format document/selection** commands insert/remove spaces, indentation and newlines to make code uniformly formatted. See also **Options > Code editor > Formatting**.

## Comment/uncomment/indent/unindent lines

To disable or enable a line of code by converting it to/from comments, you can use the toolbar button or **Edit** menu or right-click the selection margin. If multiple lines are selected, it converts all. If not full line(s) selected, the button uses a `/*block comment*/`.

Press `Tab` or `Shift+Tab` to indent or unindent all selected lines. It adds or removes one tab character before each line.

## Capture UI elements, insert regex etc, implement interface

The **Code** and **Edit** menus contain tools for creating code to find a window, UI element or image, for inserting parts of regular expression or keys string, generating interface/abstract implementation methods, and more.

## Find Windows API and insert declarations

The app comes with a database of Windows API declarations, and helps to find and insert them. More info: menu **Code > Windows API**, click **[?]**.

## Drag and drop files to insert path

You can drag and drop files from File Explorer etc to the code editor. It inserts code with file path. Links too.

You can also drag and drop scripts etc from the Files panel.

## Focus

To focus the code editor control without changing selection: middle-click.
