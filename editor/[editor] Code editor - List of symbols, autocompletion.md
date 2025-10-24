# Code editor - List of symbols, autocompletion

When you start typing a word, editor shows a list of symbols (classes, functions, variables, C# keywords, etc) available there. Or you can press `Ctrl+Space` to show the list anywhere.

The list shows only items that contain the partially typed text. The text in list items is highlighted. Auto-selects an item that is considered the first best match. On `Ctrl+Space` shows all. You can use the vertical toolbar to filter and group list items, for example to show only methods.

While the list is visible, when you double-click an item or press `Enter`, `Tab`, `Spacebar` or type a non-word character, the partially or fully typed word is replaced with the text of the selected list item. Also may add `()`, for example if the word is a function name or a keyword like `if`. By default adds `()` only if completed with `Spacebar`; see **Options > Code**.

To select list items you also can click or press arrow or page keys. It does not hide the list. The tooltip-like window next to the list shows more info about the selected item, including links to online documentation and source code if available. Shows all overloads (functions with same name but different parameters), and you can click them to view their info.

To hide the list without inserting item text you can press `Esc` or click somewhere in code.

While the list is visible, you can press the **[+]** button or `Ctrl+Space` to show another list that includes all types or extension methods, not only those from `using` namespaces.