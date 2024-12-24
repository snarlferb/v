### Normal Mode Panel
`Backspace`    -  moves back a character

`Return`       -  cursor goes down to the beginning of the next line

`Ctrl+RorLEFT`  -  jump to beginning of non-whitespace character

`Ctrl+q`       -  behaves like visual-block

`q/` and `q:`    -  pressing q: while in normal mode opens command-line history, same with q/ search history

`q`            -  recording/exit recording

`qa`           -  record macro to a register of choice

`@a`           -  e.g. run macro 'a'

`@@`           -  rerun last macro

`w`            -  moves cursor forward to beginning of a char/word

`Shift+W`      -  same as w, except more deliberate

`e`            -  moves cursor forward to end of a word

`Shift+E`      -  same as e, except more deliberate

`r`            -  replaces char with any following char

`Shift+R`      -  replace mode continually until <ESC>

`Ctrl+r`       -  redo an undo

`Ctrl+r+0`     -  allows you to paste into search

`t`            -  (motion) moves cursor before a given char

`Shift+T`      -  (motion) moves cursor backwards before a given char

`yy`           -  yank

`Shift+Y`      -  yank line and go to beginning of line

``y`a``          -  yank to mark a

`"3y`          -  yank to (e.g. register 3)

`u`            -  undo

`Shift+U`      -  restore last changed

`p`            -  paste clipboard after cursor

`Shift+p`      -  paste clipboard before cursor

`"3p`          -  paste from (e.g. register 3)

`s`            -  delete/substitute char, insert mode

`Shift+S`      -  delete/substitute line, insert mode

`f`            -  jumps to the next occurrence of any proceeding char

`Shift+F`      -  jumps back to the char

`ge`           -  moves cursor backwards to the end of a word

`gf`           -  go to file on cursor

`gg`           -  go to first line of the document

`Shift+G`      -  go to last line of the document

`gJ`           -  join line below-to the end of the current line

`~`            -  switch upper/lowercase

`g~`           -  switch upper/lowercase, motion w/direction

`gu`           -  change to lowercase, motion w/direction

`gU`           -  change to uppercase, motion w/direction

`g,`           -  go to newer position in change list

`g;`           -  go to older position in change list

`gd`           -  go to first occurrence of file/word

`Ctrl+g`       -  see information such as name of file, @statusbar

`h`            -  moves cursor left (or to a certain number of character backwards in the line, e.g. 80h)

`|`            -  by itself, moves the cursor to the first character of a given passage. but it can be us as e.g. `360|` to move to a certain number of characters in—spanning multiple lines

`vipJ`         -  joins all lines in the paragraph (the vip selects the paragraph, and J joins the lines)

`Shift+H`      -  moves cursor screen top

`j`            -  moves cursor down

`Shift+J`      -  backspace an EOL under the cursor

`k`            -  moves cursor up

`Shift+K`      -  open manpage for word under cursor

`l`            -  moves cursor right (or to a certain number of characters in that line, e.g. 80l

`Shift+L`      -  moves cursor screen bottom

`zz`           -  center cursor on screen

`Shift+ZZ`     -  save and exit immediately

`Shift+ZQ`     -  exit without saving

`Shift+WQ`     -  exit (circumstancially saved)

`zt`           -  position screen w/ cursor's position as top-most

`zb`           -  position screen w/ cursor's position as bottom-most

`x`            -  xdelete char ahead of the cursor

`Shift+X`      -  xdelete char behind the cursor, subsequently moving the cursor back

`d`            -  motion delete (including EOL) w/ direction, 'd' for selection, or number to delete

`Shift+D`      -  delete starting from cursor to last character of a line (can be customized to DelVisualBlackhole register)

`dw`           -  deletes all char/whitespace right of the cursor and beginning of the leading char/whitespace

`diw`          -  deletes all char/whitespace while positioned at the first non-space character

`d0`           -  deletes everything to the left of the cursor while positioned at the first non-space character

`da"`          -  (example of) deleting everything, as well as (quotation marks)

`dap`          -  delete around paragraph

`di"`          -  (example of) deleting everything in between (quotation marks)

`c`            -  motion cut/change whole line

`Shift+C`      -  cut/change on cursor up to last character of a line, insert mode

`c$`           -  cut/change on cursor up to last character of a line, insert mode

`ce`           -  cut/change on cursor up to end of word, insert mode

`cc`           -  cut/change line, insert mode

`ci"`          -  (example of) changing everything in between (quotation marks), insert mode

`ci(`          -  change inner parentheses

`cw`           -  at beginning of word, change word (delete, insert mode)

`ciw`          -  same behavior as diw/, insert mode

`viw`          -  select word

`b`            -  moves cursor backwards to the start of a word

`Shift+B`      -  moves cursor backwards to the start of a word (ignores alt-characters)

`Shift+RIGHT`  -  same as w

`Shift+LEFT`   -  same as b

`Shift+UP`     -  same as PgUp

`Shift+DOWN`   -  same as PgDn

`5 + DOWN`   -  move cursor down (e.g. 5) characters

`Ctrl+n`       -  same as j

`n`            -  repeat search in same directory

`Shift+N`      -  repeat search in opposite direction

`m`            -  DOESNT DO ANYTHING, ASSIGN SOMETHING TO IT!...

`Shift+M`      -  moves cursor middle of screen

`ma`           -  set current position for mark a

`{`            -  moves up by paragraph (or function block when editing)

`{`            -  moves up by paragraph (or function block when editing)

`(`            -  moves up by ?

`)`            -  moves down by ?

`-`            -  same as k

`==`           -  align back to beginning

`;`            -  repeat previous f,t,F,T movement

`,`            -  repeat previous f,t,F,T movement, backwards

`'a`           -  jump to same line as mark a

`backtick a`           -  jump to position of mark a

`backtick '`           -  jump to the previous position of the cursor

`0`           -  jump to the start of a line

`backtick 0`           -  jump to previous exit position in vim

`backtick .`           -  jump to position of last change/write

`backtick backtick`           -  jump to position and a previously made position

`#`            -  highlights all word(s) the cursor is on

`*`            -  highlights all word(s) the cursor is on & jumps to first occurrence

`$`            -  jump to last character of a line

`%`            -  move to matching braces, bracket or Parentheses

`&`            -  find pattern

`^`            -  move to the first non blank character of a line

`Ctrl+^`       -  go to last screen... (another trick i like to use is searching for `/\..\/` to quickly go back any amount of levels)

`.`            -  repeat last command

`>>`         - moves right by a space(s)(..difficulties on empty line) similaritiesw/ v + < or >

`<<`         - moves left by a space(s)

`Ctrl+v+ tab`  - While in [Insert Mode] will insert a tab



`Ctrl+e`       - move screen one line down

`Ctrl+y`       - move screen one line up

`Ctrl+u`       - move screen up 1/2 (cursor moves 1/2 w the screen, marked at the same distance of the screen)

`Ctrl+d`       - move screen down 1/2 (cursor moves 1/2 w the screen, marked at the same distance of the screen)

`Ctrl+f`       - move one full screen down

`Ctrl+b`       - move one full screen up



### [Ex]Command Mode Panel

:ex  commands    :marks     :ju[mps]    etc. (s[om]e wo[rd] brackets are being used as visual/mnemonic aids)

quick note, that pressing `:` while in visual mode puts you into ex mode and populates it w/ `:'<,'>` which represents the range of lines that your visual selection covers.

e.g. `:%s/\<yadayada\>//g`  - deletes all occurrences of yadayada w/ safety

e.g. `:%s/yada//g`          - deletes yada within all occurrences of yadayada

e.g. `:%s/YADA/yada/g`      - replace all occurrences of YADA w/ yada

e.g. `:42,86y`   - specifies a range of lines to yank

e.g. `:32,46d`   - specifies a range of lines to delete

`:.=`       - number of line at cursor, @statusbar

`/pattern`       - search for pattern

`?pattern`       - search backward for pattern

`\vpattern`      - 'very magic' pattern:

*Non-alphanumeric characters are interpreted as special regex symbols (no escaping needed)*
*However, there are cases where you need to escape some symbol to interpet them literally.*

`:vim /pattern/ {{file}}` - search for pattern in multiple files

e.g. `:vim /foo/ **/*`

`:cn[ext]` - jump to the next match

`:cp[revious]` - jump to the previous match

`:cope[n]` - open a window containing the list of matches

`:ccl[ose]` - close the quickfix window

`:e[dit] file` - edit a file in a new buffer

`:bn[ext]` - go to the next buffer

`:bp[revious]` - go to the previous buffer

`:bd[elete]` - delete a buffer (close a file)

`:b[uffer]#` - go to a buffer by index #

`:b[uffer] file` - go to a buffer by file

`:ls or :buffers` - list all open buffers

`:sp[lit] file` - open a file in a new buffer and split window

`:vs[plit] file` - open a file in a new buffer and vertically split window

`:vert[ical] ba[ll]` - edit all buffers as vertical windows

`:tab ba[ll]` - edit all buffers as tabs

`Ctrl + ws` - split window

`Ctrl + wv` - split window vertically

`Ctrl + ww` - switch windows

`Ctrl + wq` - quit a window

`Ctrl + wx` - exchange current window with next one

`Ctrl + w=` - make all windows equal height & width

`Ctrl + wh` - move cursor to the left window (vertical split)

`Ctrl + wl` - move cursor to the right window (vertical split)

`Ctrl + wj` - move cursor to the window below (horizontal split)

`Ctrl + wk` - move cursor to the window above (horizontal split)

`Ctrl + wH` - make current window full height at far left (leftmost vertical window)

`Ctrl + wL` - make current window full height at far right (rightmost vertical window)

`Ctrl + wJ` - make current window full width at the very bottom (bottommost horizontal window)

`Ctrl + wK` - make current window full width at the very top (topmost horizontal window)

`]c`        - jump to start of next change

`[c`        - jump to start of previous change

`do or :diffg[et]` - obtain (get) difference (from other buffer)

`dp or :diffpu[t]` - put difference (to other buffer)

`:diffthis` - make current window part of diff

`:dif[fupdate]` - update differences

`:diffo[ff]` - switch off diff mode for current window

`:registers` - list of registers

`:scriptnames` - list all the sourced script names (plus last sourced line#)

`:filetype`  - displays current filetype detection settings

`:term`      - open terminal

`:set`       - displays current option settings



### Insert Mode Panel from Normal Mode

`i`            -  insert before cursor

`Shift+I`      -  insert to beginning of line

`a`            -  insert after cursor

`Shift+A`      -  insert to end of the line

`o`            -  insert into a newline after current line

`Shift+O`      -  insert into a newline before current line

### Insert Mode Panel from Insert

`TAB`          - can produce space(s) or a tab

`Ctrl+^`       - go back to previous file

`Ctrl+q...`    - starts a 'Control' command

`Ctrl+w`       - deletes a character

`Ctrl+e`       - mimics the character thats 'below' the cursor

`Ctrl+r`       - replace mode (r to insert it)   

`Ctrl+t`       - indent >>

`Ctrl+y`       - circular duplication of each character in sequence

`Ctrl+u`       - deletes everything from beginning to position

`Ctrl+i`       - behaves like spacebar

`Ctrl+o`       - command-&gt;insert imitation, mode-swap

`Ctrl+p`       - dropdown list of words

`Ctrl+d`       - indent <<

`Ctrl+a`       - replaces the previous character with current

`Ctrl+s`       - ^S 

`Ctrl+f`       - ^F

`Ctrl+j`       - behaves like carriage return

`Ctrl+k`       - motion for special characters, etc

`Ctrl+l`       - ^L

`Ctrl+z`       - ^Z

`Ctrl+x`       - ^X mode

`Ctrl+v`       - motion control characters

`Ctrl+b`       - ^B

`Ctrl+n`       - dropdown list of words similar to the word at cursor

`Ctrl+m`       - behaves like carriage return

`Ctrl+\`       - ^\

`Ctrl+Backspace`       - ^?

`Ctrl+Shift+Hyphen` - ^_

`Ctrl+backtick`    - outputs a backtick character, and exits to normal mode (actually kindve annoying)

`Ctrl+Shift+backtick`    - does nothing



### Visual Mode Panel from Normal Mode

`v`            - visual (regular)

`Shift+V`      - visual line

`Ctrl+v`       - visual block



### Special Mode Panels

**Very No Magic Mode**:

- It requires a specific sequence. Start by yanking a visual selection as you normally would.
- Then type `/` for the search prompt, and type  `\V` , immediately after you type `"` a quote and press enter.



**Blockwise Visual Mode**:

- Ctrl+v (and proceed to select a column/block of text) and **<Key>**`Shift+I` Which you then proceed to do *some action*.
- Afterwards, press *exit* twice, and you will have performed that action for the entire column of text.. and presumably
you could also paste from your cursor location into the bespoke column, and the *selected text* will be altered based
on whichever action you choose.



**Register Behavior**:
They are storage locations for strings in some sense.

Vim automatically stores the text of the last yank operation in the "0 register as well as the " unnamed register (default register).
But it should also be noted that the register behavior has changed since version 9.0, and although i do not know all the changes,
i can say that - what use to be the intended behavior of register 1, 2, 3 etc.. is now different, and could only be reproduced
using a, b, c, etc...

I could be wrong about the details of *which* registers... but if you try yanking a visual block of text and
pasting, you'll notice its the reverse case - that "0 no longer is responsible for filling multi-selected visual block lines w/ a
character(s), and that whichever register did the ladder now behaves in the opposite way, and vice versa. I just havent yet tested
what all those registers are.

1 to 9 (shifting delete registers, when you use commands such as c or d, what has been deleted goes to register 1,
what was in register 1 goes to register 2, etc.),



Paste Yanked Text Into :Command Line or :/Search

In Insert or Command-line mode, Ctrl-R plus a register name, inserts the content of that register. 
That is, you use   :Ctrl+r, Ctrl+o, and register name, which pastes it literally to :command-line
You can use Ctrl+o after in order to continue typing additional text after pasting into the prompt.

To make sure it goes into search its :/Ctrl+r, and register name. Hit [Enter]



Universal Clipboard w/ XClip

`set clipboard=unnamedplus`          - must be in `~/.vimrc`, as it allows yank/paste w/ register `"+y` 

`xclip -o`                           - to paste into CLI

`help command | xclip -sel c`        - pipes to clipboard (directly from file to clipboard)

`xclip -sel c < /path/to/file. c`    - self explanatory

`:'<,'>w !xclip -sel c`              - yank currently selected text to clipboard



Paste Unicode Characters

Characters that are not part of the standard ASCII set can be accessed in vim easily through the following &lt;Key&gt;sequence while in INSERT mode.
You can find a list of more Unicode characters and their corresponding code points in various online resources or Unicode tables:

e.g.  Ctrl v  u  2014                - inserts a long dash or hyphen, i.e. "—"



Again, Vim has many many more key commands and ways to manipulate keys and commands...
And its often the case that you employ some of the custom configurations from within
the resource configuraton file to tailor it to your liking.

p.s. vim is constantly receiving updates, and so you may often find some things broke  or
those things that were previously broken  now  fixed  and vice versa, so you should try
to stay up-to-date with the latest version if you care about having the latest/greatest.

