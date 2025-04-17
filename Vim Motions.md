S - insert mode but it removes the current line
:xq - save and quit -> you can stack commands together
:r {filename} will insert another file into the current file
:vsplit {file name} - opens 2 files in 1 window
Ctrl + ww - moves to the next file that's open

ctrl + 0 - puts you in normal mode for 1 command
:%s/{text to replace}/{new text}/g - find

gg - takes you to top
shift + g - takes you to end

Select lines, press `>` to indent!
`<C-n>` :  show suggestions (sorta, but not quite)
 `C-V` Visual Block Mode - select lines, then press Shift I to insert, then press Esc and it will insert to all lines.

ZZ - does it quit?
:normal A;
:%normal A;    - do for every line
:'<,'>normal A;   - visual selections only
`:'<,'>v/;$/normal A;`   - Or on particular lines, according to regex (add a semi-colon to visually-selected lines that don't end with a semicolon)
`:%norm ysil"A,` A more practical example, just to show why I prefer this method. This uses vim-surround and text-object-line to quote the range of lines and put a comma after (useful for turning a list of lines into a JSON array):


---
f and t - finds & includes a character in the current line (F jumps back)
**dfs - delete everything up until the letter s in the line.**
**dt" - delete everything up to (not including) the letter " in the line.**
yiw - yank word under the cursor
**diw - del word under the cursor**
daw - del word under the cursor and the space next to it
yy - yank a line
<> - shift text left / right
+y - copy thinks to the clipboard on Mac
**diW- delete the entire thing** 

init.vim:
set number
set relativenumber

```
h j k l : w W e E b B x X r d dd D ~ 0 ^ $ f F t T ; , % z zt zz zb g gg G  
digits (1-9) * # n N p P " y yy Y :reg "" "- "_ numbered-registers  
letter-registers i I a A c cc C s S o O { } ( ) [{ ]} [( ]) . text-objects  
H M L nu | / ? ` ' m :marks :delmarks u CTRL-R buffers (:b :ls) files (:w :e)
+ - macros (q @) rnu
```
---
[^1]: https://www.youtube.com/watch?v=5JGVtttuDQA&list=PLm323Lc7iSW_wuxqmKx_xxNtJC_hJbQ7R&index=7
[^2]: https://www.youtube.com/watch?v=h4ZQfr-q3EA - Mostly Summarized, but there's still some config stuff i should do
[^3]: [Vim Cheat Sheet](https://vim.rtorr.com)
[^4]: https://vim-adventures.com/ - Finished