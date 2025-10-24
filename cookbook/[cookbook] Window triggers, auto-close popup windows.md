# Window triggers, auto-close popup windows

To execute some code or run a script, can be used window [triggers](/api/Au.Triggers.ActionTriggers.html). For example auto-close popup window X whenever it appears.

To add a trigger can be used snippet `triggerSnippet` or `Ctrl+Shift+Q` or menu **TT > New trigger**. Add triggers in function `WindowTriggers` in file `Window triggers`; you'll find examples there.

To open a triggers file for editing can be used the **TT** menu.

Click the **Run** button to apply changes after editing.

Tips:

- Most window trigger parameters are the same as with `wnd.find`. To get window name etc can be used the **Find window** tool or Quick capturing (`Ctrl+Shift+Q`).
- To get code for "run script" or "run/open file or URL" you can drag and drop scripts, files and links to the code editor.

See also recipe [Triggers and toolbars](Script%20%27Triggers%20and%20toolbars%27.html).

Also triggers can be used in any script. For example in an `.exe` program that runs without the editor. [Examples](/api/Au.Triggers.ActionTriggers.html).