# Code editor - Highlight symbol references and matching braces

When the text cursor is in a symbol name, the editor automatically highlights that name everywhere in current document.

When the text cursor is before an opening brace `({[<`, highlights the matching closing brace `)}]>`. When after a closing brace, highlights the matching opening brace. When at the `#` of `#if` etc, highlights matching `#endif` etc.

To turn off these features: **Options > Font, colors > Symbol/brace highlight**, set color white and alpha 0.