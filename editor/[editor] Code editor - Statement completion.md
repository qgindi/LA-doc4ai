# Code editor - Statement completion

When you press `Enter` immediately before `)`, `]` or `;`, editor adds missing `;` or `{ }`, adds new line, moves the text cursor, and formats the statement. Except if before is `,` or space character.

However the above feature interferes with writing multi-line statements. Ways to bypass it:

- Disable temporarily: toggle **Raw Enter before ) ] ;** on the toolbar.
- Use `Shift+Enter`. Or `Ctrl+Enter`, depending on settings.
- Type space before `Enter`.
- `Enter` and `Ctrl+Z` (undo). It undoes the change and adds new line inside the statement.
- You can continue a vertical method chain by typing `.` on the next line after the `;`.
- If you never need this feature, disable it in **Options**.

Use hotkey `Ctrl+Enter` (can be changed in **Options**) to complete current statement when the text cursor is anywhere in it. Also it can add `{ }` to `class C` etc.

Also completes statement on `Enter` in a single-line `"string"` or `"""string"""`, unless the text cursor is at `"""|text"""`.

To complete statement without new line, use `;` instead of `Enter`. It adds `;` if missing, moves the text cursor, and formats the statement. With `Ctrl` it works anywhere in the statement; without - only before `)` or `]`.

As you begin typing a statement (eg a word in a blank line), editor adds `;`. Later deletes if don't need (eg when completing with `{ }`) or overtypes `;` with `;`. This feature can be disabled in **Options**.

You can use `Backspace` to exit current multiline `{ block }` when the text cursor is in the last line of the block and that line is blank.