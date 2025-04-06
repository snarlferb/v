### Normal Mode

Lets first establish some things about opening and closing Vim, as thats a very popular meme.

To open a file(s):
`vim filename1 filename 2`

Or simply opening the current directory `vim ./` will bring you into the netrw directory view.

Use `vim -c ":help"` to launch into the built-in help system from the command line, or the `:help` or `:help <topic>`
while already inside. If you have any open splits or windows, you can close them to make the help view take up the entire screen
`:only`

If you are already in Vim and want to open another file, you can use the following (we'll talk more about the ex `:` command mode later on)
`:e filename`

To quit out of Vim (w/ unsaved or blank file) you'd use the `:q` command
If there are multiple files (windows) open, you can use `:qa` (Vim will prompt you to save or discard them)
And if you have unsaved changes, but need to force quit you'd use the `:q!` command,
or in the case of forcing out of multiple files, its `:qa!`

While in normal mode, you can also use the shortcut: `Shift ZQ`. To save changes to the current file (`:w`), or to save and
then quit, you can use either `:wq` or `:x` ... or `Shift ZZ` is the shortcut. These close the **currently selected window** only.

> This is the end of the keys and shortcuts guide for opening or quitting/closing (or exiting Vim)
____

A buffer is simply an in-memory representation of a file. Vim keeps track of the files you open as "buffers".
To see a list of all open buffers, use the `:ls` command.

To switch between buffers, you can use for example:
`:b 2` which switch to buffer 2, assuming you even have a second buffer open. Likewise...
`:bd` would close buffer 2
`:b filename` is when you know that buffer (files) name
`:bufdo bd` is for closing all buffers
`:bnext` is to switch to the next buffer, and
`:bprev` is to switch tot he previous

We'll talk about windows and tabs later, however to just briefly explain the difference—going in order: Buffers are files, Windows
are views of those buffers that allows you to split and navigate through each, etc., and "Tabs" are collections of windows, allowing you
to have multiple layouts within a single Vim session.

To save your current Vim session, use the `:mksession` command, e.g.
`:mksession mysession.vim`

To restore a saved session, you can start Vim with the session file using the -S option:
`vim -S mysession.vim`

Alternatively, you can load the session from within w/:
`:source mysession.vim`

You can set Vim to automatically save and restore your session when opening and closing Vim, alas that's getting too much into configuration files.

A Vim session is a culmination of all the aforementioned history, as well as any Open files (buffers), windows (splits), Tab pages (if
you're using tabs), the cursor position of the file in question, and any other information about the state that you were preserving.

> This is the beginning of the command and shortcut list, and all of its subsequent modes, starting w/ Normal Mode (not to be confused w/ XTerm's Normal Mode)
____

*Note: I sometimes write out the word `backtick` when i cannot preserve multiple backticks in a single code block (an unfortunate quark of markdown)*

`Backspace`    -  moves back a character

`Return`       -  cursor goes down to the beginning of the next line

`Ctrl RorLEFT`  -  jump to beginning of non-whitespace character

`Ctrl q`       -  behaves like visual-block

`q/` and `q:`    -  pressing q: while in normal mode opens command-line history, same with q/ search history

`q`            -  recording/exit recording

`qa`           -  record macro to a register of choice

`@a`           -  e.g. run macro 'a'

`@@`           -  rerun last macro

`w`            -  moves cursor forward to beginning of a char/word

`Shift W`      -  same as w, except more deliberate

`e`            -  moves cursor forward to end of a word

`Shift E`      -  same as e, except more deliberate

`r`            -  replaces char with any following char

`Shift R`      -  replace mode continually until <ESC>

`Ctrl r`       -  redo an undo

`Ctrl r 0`     -  allows you to paste into search

`t`            -  (motion) moves cursor before a given char

`Shift T`      -  (motion) moves cursor backwards before a given char

`yt`           -  yank from the current cursor position up to just before x (or whatever character is specified)

`yy`           -  yank

`Shift Y`      -  yank line and go to beginning of line

``y`a``          -  yank to mark a

`"3y`          -  yank to (e.g. register 3)

`u`            -  undo

`Shift U`      -  restore last changed

`p`            -  paste clipboard after cursor

`Shift P`      -  paste clipboard before cursor

`"3p`          -  paste from (e.g. register 3)

`s`            -  delete/substitute char, insert mode

`Shift S`      -  delete/substitute line, insert mode

`f`            -  jumps to the next occurrence of any proceeding char

`Shift F`      -  jumps back to the char

`ge`           -  moves cursor backwards to the end of a word

`gf`           -  go to file on cursor

`gg`           -  go to first line of the document

`Shift G`      -  go to last line of the document

`gJ`           -  join line below-to the end of the current line

`~`            -  switch upper/lowercase

`g~`           -  switch upper/lowercase, motion w/direction

`gu`           -  change to lowercase, motion w/direction

`gU`           -  change to uppercase, motion w/direction

`g,`           -  go to newer position in change list

`g;`           -  go to older position in change list

`gd`           -  go to first occurrence of file/word

`Ctrl g`       -  see information such as name of file, @statusbar

`g?`           -  this turns a selection into rot13 cipher text, where: given the alphabet starts at 0, then (x+13)mod(26) each character

`h`            -  moves cursor left (or to a certain number of character backwards in the line, e.g. 80h)

`|`            -  by itself, moves the cursor to the first character of a given passage. but it can be us as e.g. `360|` to move to a certain number of characters in—spanning multiple lines

`vipJ`         -  joins all lines in the paragraph (the vip selects the paragraph, and J joins the lines)

`Shift H`      -  moves cursor screen top

`j`            -  moves cursor down

`Shift J`      -  backspace an EOL under the cursor

`k`            -  moves cursor up

`Shift K`      -  open manpage for word under cursor

`l`            -  moves cursor right (or to a certain number of characters in that line, e.g. 80l

`Shift L`      -  moves cursor screen bottom

`zz`           -  center cursor on screen

`Shift ZZ`     -  save and exit immediately

`Shift ZQ`     -  exit without saving

`Shift WQ`     -  exit (circumstancially saved)

`zt`           -  position screen w/ cursor's position as top-most

`zb`           -  position screen w/ cursor's position as bottom-most

`x`            -  xdelete char ahead of the cursor

`xp`           -  transpose the character under the cursor w/ the proceeding char

`Shift X`      -  xdelete char behind the cursor, subsequently moving the cursor back

`d`            -  motion delete (including EOL) w/ direction, 'd' for selection, or number to delete

`Shift D`      -  delete starting from cursor to last character of a line (can be customized to DelVisualBlackhole register)

`dw`           -  deletes all char/whitespace right of the cursor and beginning of the leading char/whitespace

`diw`          -  deletes all char/whitespace while positioned at the first non-space character

`d0`           -  deletes everything to the left of the cursor while positioned at the first non-space character

`da"`          -  (example of) deleting everything, as well as (quotation marks)

`dap`          -  delete around paragraph

`di"`          -  (example of) deleting everything in between (quotation marks)

`c`            -  motion cut/change whole line

`Shift C`      -  cut/change on cursor up to last character of a line, insert mode

`c$`           -  cut/change on cursor up to last character of a line, insert mode

`ce`           -  cut/change on cursor up to end of word, insert mode

`cc`           -  cut/change line, insert mode

`ci"`          -  (example of) changing everything in between (quotation marks), insert mode

`ci(`          -  change inner parentheses

`cw`           -  at beginning of word, change word (delete, insert mode)

`ciw`          -  same behavior as diw/, insert mode

`viw`          -  select word

`b`            -  moves cursor backwards to the start of a word

`Shift B`      -  moves cursor backwards to the start of a word (ignores alt-characters)

`Shift RIGHT`  -  same as w

`Shift LEFT`   -  same as b

`Shift UP`     -  same as PgUp

`Shift DOWN`   -  same as PgDn

`5   DOWN`   -  move cursor down (e.g. 5) characters

`Ctrl n`       -  same as j

`n`            -  repeat search in same directory

`Shift N`      -  repeat search in opposite direction

`m`            -  DOESNT DO ANYTHING, ASSIGN SOMETHING TO IT!...

`Shift M`      -  moves cursor middle of screen

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

`Ctrl ^`       -  go to last screen... (another trick i like to use is searching for `/\..\/` to quickly go back any amount of levels)

`.`            -  repeat last command

`>>`         - moves right by a space(s)(..difficulties on empty line) similaritiesw/ v + < or >

`<<`         - moves left by a space(s)

`Ctrl v tab`  - While in [Insert Mode] will insert a tab



`Ctrl e`       - move screen one line down

`Ctrl y`       - move screen one line up

`Ctrl u`       - move screen up 1/2 (cursor moves 1/2 w the screen, marked at the same distance of the screen)

`Ctrl d`       - move screen down 1/2 (cursor moves 1/2 w the screen, marked at the same distance of the screen)

`Ctrl f`       - move one full screen down

`Ctrl b`       - move one full screen up



### [Ex] versus Reg/\Ex Command Mode(s)

:ex  commands    :marks     :ju[mps]    etc. (s[om]e wo[rd] brackets are being used as visual/mnemonic aids)

Quick note, that pressing `:` while in visual mode (w/ a visual selection) puts you into ex mode and populates it w/ `:'<,'>` which is just the shortcut Vim uses to pass a visual selection to commands. its almost like telling the program, *"Do so and so command that falls after `'<,'>`, but make sure it is  relative to selected text that it finds after execution."*  I use the mneumonic  ALBACARBtuna  to remember when writing it freehand (you can also specify a range of lines, which we'll go into that stuff as we go)

Ex mode is different from reg/\ex mode, and substitution aka "search and replace" — You also have commands you can perform like `:g` or "global"—begin while in the Ex mode. And, while in Ex. you can enter normal mode, and normal mode commands —> `:norm[al] [command]`. And btw, ALL of these commands are like individual puzzle pieces, and they can be used together to create more elaborate commands (you'll also notice that Vim's normal mode command(s) are a running motif and often make an appearance)

Now you can press `Ctrl v` then `Esc` to insert a literal escape character, and it'll appear as `^[` (the equivalent of pressing the Esc key) during the sequence of writing said Ex command. It doesnt have to be ESC though, for example: `Ctrl v` and `Ctrl m` inserts a carriage return (`^M`), or `Ctrl v` and `Tab` inserts a tab character (`^I`) (we'll be including more about control characters)

e.g. `:g/^$/,/^$/-1 join`       - to merge lines into proper paragraphs (preserving blank lines as paragraph breaks). `/^$/` matches empty lines (lines that contain nothing), and `,/^$/-1 join` forms a range from the matched empty line (`/^$/`) to the next empty line (`/^$/`), minus one line (-1), meaning it stops at the line before the next empty one. `join` thus merges all lines in this range into one, removing the newlines in the process.

e.g. `:[range]s/pattern/replacement/[flags]`

e.g. `:s/foo/bar/`     - replace the first occurrence of "foo" w/ "bar" on the current line

e.g. `:%s/\<foo\>//g`  - deletes all occurrences of  foo  w/ safety

e.g. `:%s/foo//g`          - deletes all occurrences of  foo  found within all words

e.g. `:%s/FOO/foo/g`      - replace all occurrences of  PATTERN w/ pattern

e.g. `:42,86y`   - specifies a range of lines to yank

e.g. `:32,46d`   - specifies a range of lines to delete

`:.=`       - number of line at cursor, @statusbar

`/pattern`       - search for  pattern

`?pattern`       - search backward for  pattern

`/\<pattern\>`   - search for  pattern  as it exists as a word, as opposed to all instances of

`\vpattern`      - 'very magic' pattern: Non-alphanumeric characters are interpreted as special regex symbols (no escaping needed)
                    However, there are cases where you need to escape some symbol to interpet them literally.*

Notice, the "very magic" search pattern can be used w/ any regex/substitution variations, or anytime regex becomes overly complex or
hard to read due to escaping. It’s especially useful for more readable and concise patterns during searches or substitutions.

Also keep in mind these commands can be employed in the context of a script—building individual ex programs—either in `.vimrc` for reusable code, or as plugins.

`:call` command is one such example, as its used to call (execute) a function that you’ve defined (or to invoke an existing function)

`:vim /pattern/ {{file}}` - search for  pattern  in multiple files, e.g. `:vim /foo/ **/*`

`**/*` → is a glob pattern that matches all files recursively,

`**` means "all directories and subdirectories"

`*` means "all files within those directories"

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

`:tab ba[ll]` - edit all buffers as tabs (inb4, `:tabnew`, `:tabnext`, `:tabprev` and `:tabclose`)

`Ctrl  ws` - split window

`Ctrl  wv` - split window vertically

`Ctrl  ww` - switch windows

`Ctrl  wq` - quit a window

`Ctrl  wx` - exchange current window with next one

`Ctrl  w=` - make all windows equal height & width

`Ctrl  wh` - move cursor to the left window (vertical split)

`Ctrl  wl` - move cursor to the right window (vertical split)

`Ctrl  wj` - move cursor to the window below (horizontal split)

`Ctrl  wk` - move cursor to the window above (horizontal split)

`Ctrl  wH` - make current window full height at far left (leftmost vertical window)

`Ctrl  wL` - make current window full height at far right (rightmost vertical window)

`Ctrl  wJ` - make current window full width at the very bottom (bottommost horizontal window)

`Ctrl  wK` - make current window full width at the very top (topmost horizontal window)

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

`:execute`   - build and run commands

`:redir`     - captures command output

`:term`      - open terminal

`:set`       - displays current option settings

`:let`       - assigns values to variables



### Insert Mode from Normal Mode

`i`            -  insert before cursor

`Shift I`      -  insert to beginning of line

`a`            -  insert after cursor

`Shift A`      -  insert to end of the line

`o`            -  insert into a newline after current line

`Shift O`      -  insert into a newline before current line

### Insert Mode (Control Commands)

`TAB`          - can produce space(s) or a tab

`Ctrl ^`       - go back to previous file

`Ctrl q...`    - starts a 'Control' command

`Ctrl w`       - deletes a character

`Ctrl e`       - mimics the character thats 'below' the cursor

`Ctrl r`       - replace mode (r to insert it)   

`Ctrl t`       - indent >>

`Ctrl y`       - circular duplication of each character in sequence

`Ctrl u`       - deletes everything from beginning to position

`Ctrl i`       - behaves like spacebar

`Ctrl o`       - command-&gt;insert imitation, mode-swap

`Ctrl p`       - dropdown list of words

`Ctrl d`       - indent <<

`Ctrl a`       - replaces the previous character with current

`Ctrl s`       - ^S 

`Ctrl f`       - ^F

`Ctrl j`       - behaves like carriage return

`Ctrl k`       - motion for special characters, etc

`Ctrl l`       - ^L

`Ctrl z`       - ^Z

`Ctrl x`       - ^X mode

`Ctrl v`       - motion control characters

`Ctrl b`       - ^B

`Ctrl n`       - dropdown list of words similar to the word at cursor

`Ctrl m`       - behaves like carriage return

`Ctrl \`       - ^\

`Ctrl Backspace`       - ^?

`Ctrl Shift Hyphen` - ^_

`Ctrl backtick`    - outputs a backtick character, and exits to normal mode (actually kindve annoying)

`Ctrl Shift backtick`    - does nothing



### Visual Mode from Normal Mode

`v`            - visual (regular)

`Shift V`      - visual line

`Ctrl v`       - visual block



### Other Special Mode(s)

**Paste Yanked Text Into, e.g. :Command Line or :/Search**

- You start by yanking the text you want to use.
- In Insert or Command-line mode, `Ctrl r` plus a register name, inserts the content of that register. 
- That is, you use   `:Ctrl r`, `Ctrl o`, and register name, which pastes it literally to :command-line
- You can use `Ctrl o` after in order to continue typing additional text after pasting into the prompt.

- So the following command pastes the yanked text into the search prompt.
`/ (Ctrl r) "`

- Or to make sure it goes into search using regex, it's `:/Ctrl r`, and register name. Hit [Enter]



**Very No Magic Mode**:

- Start by yanking a visual selection as you normally would.
- Then type `/` for the search prompt, and type  `\V`  and then `Ctrl r`, followed by `"` to insert the contents of the register you just yanked.



**What is a Word Boundary**

- A word boundary is a position in the text where a word character (letters, digits, or underscores: [a-zA-Z0-9_]) is adjacent to
a non-word character (e.g., spaces, punctuation) or the start/end of the line. It marks the "edge" of a word.

- For example:  In the text  "cat caterpillar cats", a word boundary exists before "cat" and after "cat". The same is true for "cats".
- However, there is no word boundary between the " cat " and " er " in "caterpillar" because they are part of the same word.

- When you press  `*`  or  `#`  Vim extracts the word under the cursor. It constructs a search pattern that looks like this:

`\bword\b`

- But if you manually search with  `/word`  Vim does not add `\b` automatically. Here are some settings that are beneficial to use in this situation.

`:set iskeyword`   - This option defines what Vim considers a "word character"  (Default, iskeyword includes [a-zA-Z0-9_]) You can modify it
to include or exclude specific characters. For example:

`:set iskeyword+=-`   - Treats a dash  (-)  as part of a word, so `some-word` would be considered one word.
`:set ignorecase`     - Makes searches case-insensitive (You can make any search case insensitive w/, e.g. `word\c` at the end)
`:set smartcase`      - Makes searches case-sensitive only if the pattern contains uppercase letters.
`:set magic`          - Enables special regex characters (like *, +, and \b) to work naturally.
`:set nomagic`        - Treats most characters literally unless escaped (e.g., \b becomes \\b).



**Blockwise Visual Mode**:

- `Ctrl v` (and proceed to select a column/block of text) and **<Key>**`Shift+I` Which you then proceed to do *some action*.
- Afterwards, press *exit* twice, and you will have performed that action for the entire column of text.. and presumably
you could also paste from your cursor location into the bespoke column, and the *selected text* will be altered based
on whichever action you choose.



**Register Behavior**:

- They are storage locations for strings in some sense.

- Vim automatically stores the text of the last yank operation in the `"0` register as well as the `"` unnamed register (default register).
- But it should also be noted that the register behavior has changed since version 9.0, and although i do not know all the changes,
i can say that—what use to be the intended behavior of register 1, 2, 3 etc.. is now different, and could only be reproduced
using a, b, c, etc...

- I could be wrong about the details of *which* registers... but if you try yanking a visual block of text and
pasting, you'll notice its the reverse case - that "0 no longer is responsible for filling multi-selected visual block lines w/ a
character(s), and that whichever register did the ladder now behaves in the opposite way, and vice versa. I just havent yet tested
what all those registers are.

- 1 to 9 (shifting delete registers, when you use commands such as `c` or `d`, what has been deleted goes to register 1,
what was in register 1 goes to register 2, etc.)

- But in regards to behaviors around normality, `"` is used for storing and retrieving content from a register (for subsequent yank, delete, or pasted contents)
- However `@` is used for executing the commands stored in a register; Namely for repeating sequences of normal mode commands that you’ve previously stored in registers.



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

