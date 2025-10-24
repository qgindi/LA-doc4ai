# Autotext triggers, expand text

Autotext [triggers](/api/Au.Triggers.ActionTriggers.html) can be used to execute some code or auto-replace text when you type an abbreviation or an incorrectly spelled word. Also known as text expanding, auto-correction, hotstrings.

To add a trigger can be used snippet `triggerSnippet` or menu **TT > New trigger**. Add triggers in function `AutotextTriggers` in file `Autotext triggers`; you'll find examples there.

To open a triggers file for editing can be used the **TT** menu.

Click the **Run** button to apply changes after editing.

Tips:

- To get code for "run script" or "run/open file or URL" you can drag and drop scripts, files and links to the code editor.
- To quickly insert `Triggers.Of.Window(...)` code, use the quick capturing hotkey (default `Ctrl+Shift+Q`).

See also recipe [Triggers and toolbars](Script%20%27Triggers%20and%20toolbars%27.html).

Also triggers can be used in any script. For example in an `.exe` program that runs without the editor. [Examples](/api/Au.Triggers.ActionTriggers.html).