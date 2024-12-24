# v

- commands, vim9 script from this decade and a base color palette

  ### Vim modes
  Vim's considered a modal editor in the sense that its both modular by design and implementation. This means that it provides
  multiple modes and the meaning of keys changes according to the mode. You navigate files in normal mode, insert text in insert mode,
  select lines in visual mode; You also access commands in command-line mode and so on. Its really an amalgamation of modal languages
  w/ its own scripting language that defines the user-level API.
  ### Command line modes
  Ex (short for extended) is a panel (i refer to each mode as a panel) that operates on entire files, buffers, or settings.. In vim you can
  enter ex-mode `:` which'll run the ex commands. `/` Search prompt (which is a common feature in many other unix programs) is another panel
  that adds a layer to the already multilanguage accredited syntax of vim, and allows you to search using ERE, BRE and PCRE...
  If that wasnt enough, you also have Quickfix which is your own personal jump-error/search panel to jump between different
  error locations in a file, post-execution of `:make`, you do `:copen`. You can also open the terminal (w/ the configured
  terminal emulator from your shell) and run `./My-Build-Release-Program` or whatever your program is called.
  ### Conceptualizing Vim
  I like to imagine it in the same way i imagine rotating 3x3 X-O Panels at my local playground; Like curved triangles w/ qwerty layouts
  on each surface; Rotations of a panel represents changes - When you spin a panel's face you reveal a new mode. Speaking of modes,
  another tangentially-related concept are the operators and motions. Operators start a certain action, e.g. changing, removing,
  or selecting text. Afterwards you specify the region of text you want to act on w/ a motion.
  ### Limitations and Extensibility
  Vim is not without its limits. One thing it was never meant to do was string together long chains of builtin commands.
  Also, many of the things that we do w/ text editors today didnt exist at that early time Vi/Vim was made, and it was specifically
  designed to have low resource usage—so its core engine is not as dynamic as it could be. Even still, its an ever-evolving program w/
  extensions/forks and plugins. Consequently the user decides what Vim is and may extend it to their hearts desire.
