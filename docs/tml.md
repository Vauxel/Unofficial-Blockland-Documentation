# Torque Markup Language

**The Torque Markup Language is a set of specific tags that can be used to alter text in-game.**

*'__' characters are to be replaced by names, and '##' characters are to be replaced by integer values.  Additionally, text specified in parenthesis are comments on the field preceding them, and are to be removed when using that TML tag.*

#### **Effects**

`<font:__(fontname):##(fontsize)>` - Sets the font and font-size of the text.

`<color:rrggbb>` - Sets the text color specified, in hex format.

`<div:##(color)>` - Creates a grey background behind the text.

`<spush>` - Saves the current TML text formatting to allow for temporary changes to the formatting to be made.

`<spop>` - Used in conjunction with <spush> to restore the previously saved TML text formatting.

`<sbreak>` - Clears the previously saved TML text formatting.

#### **Elements**

`<a:__(url)>__(name)</a>` - Masks a hyperlink behind the text name given.

`<bitmap:__(filepath)>` - Inserts the bitmap image located at the path specified.

#### **Positioning**

`<br>` - Breaks the current line and begins a new line.

`<just:left/right/center>` - Justifies the text

`<tab:##[,##,##,##(etc)]>` - Sets tab stops at the position(s) given.

`<lmargin:##>` - Sets the left margin identation.

`<lmargin%:##>` - Sets the left margin identation by a percent of the screen.

`<rmargin:##>` - Sets the right margin identation.

`<rmargin%:##>` - Sets the right margin identation by a percent of the screen.

`<clip:##(pixelamount)>` - Cuts off the text after the amount of pixels specified has been reached.