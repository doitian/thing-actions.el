# thing-actions.el

Fast mark and move by different things

## Dependencies ##

Features that might be required by this library: `thing-cmds`, `hide-comnt`, `thingatpt`, `thingatpt+`.

## Commentary ##

I always forget key bindings to mark or move around by defun, sexp or other
text entities ("things"). So I write `thing-actions`, which defines uniform
way to mark and move by different text entities.

To use, make sure this file and `thing-cmds.el` are on your `load-path` and
put the following in your .emacs file:

    (require 'thing-actions)

Then you can bind functions like:

    (global-set-key (kbd "M-SPC") 'thing-actions-mark-thing)

Now <kbd>M-SPC</kbd> will start `thing-actions` in mark mode. Use keys defined in
`thing-actions-alist` to mark different things. Following keys will toggle
`thing-actions` in different mode:

-   <kbd>M-SPC</kbd> - mark thing, repeat the thing key to expand region.
-   <kbd>M-s</kbd>   - mark thing surround cursor
-   <kbd>M-f</kbd>   - move forward by thing
-   <kbd>M-b</kbd>   - move backward by thing
-   <kbd>M-a</kbd>   - move to the beginning of the thing surround cursor
-   <kbd>M-e</kbd>   - move to the end of the thing surround cursor

Type any key other than keys listed above and ones in `things-actions-alist` quits things-actions.

## Example ##

Suppose that `things-actions-mark-thing` is binded on <kbd>M-SPC</kbd>.

<kbd>M-SPC w w w</kbd> - mark three words, <kbd>M-3 M-SPC w</kbd> and <kbd>M-SPC M-3 w</kbd> also work.
<kbd>M-SPC M-f p</kbd> - move forward a paragraph.
<kbd>M-SPC M-a d</kbd> - move to the beginning of the defun around cursor.

## License ##

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2, or (at your option)
any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; see the file COPYING.  If not, write to the
Free Software Foundation, Inc., 59 Temple Place - Suite 330,
Boston, MA 02111-1307, USA.

