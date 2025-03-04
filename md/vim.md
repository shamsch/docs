# VIM motions I actually know and use

All of the following commands will work by default in any vim environment. I use them in VSCode primarly with occasional use in the terminal.
However, in VSCode, I like to make a few changes. Find these changes with rest of my vscode settings [here](/template.html?file=vscode.md#settings). 
> I also remap Caps Lock to Esc, but that's a system-wide setting.

## Navigation

### Character Movement
* `h` - Move cursor left
* `j` - Move cursor down
* `k` - Move cursor up
* `l` - Move cursor right

### Word Movement
* `w` - Move to start of next word
* `b` - Move to beginning of current/previous word
* `e` - Move to end of word

### Line/File Movement
* `^` - Jump to beginning of line
* `$` - Jump to end of line
* `g_` - Jump to end of line without going to next line
* `gg` - Jump to beginning of file
* `G` - Jump to end of file

### Paragraph/Sentence Movement
* `]` or `[` - Move over paragraph
* `(` or `)` - Move over sentence

### Screen Movement
* `Ctrl + u` - Move half page up
* `Ctrl + d` - Move half page down
* `Ctrl + o` - Jump back to previous location
* `Ctrl + i` - Jump forward to next location

## Modes

### Mode Switching
* `Esc` - Return to normal mode

### Insert Mode Commands
* `i` - Insert before cursor
* `a` - Insert after cursor
* `o` - Insert on new line below

### Visual Mode Commands
* `v` - Select character-wise
* `V` - Select line-wise
* `Ctrl-v` - Select block-wise
* `ggVG` - Select entire file
* `>>` - Indent selected text
* `<<` - Unindent selected text

## Text Operations

### Delete/Change/Yank (Copy)
* `x` - Delete character under cursor
* `dw` - Delete word
* `dd` - Delete entire line
* `yw` - Copy word
* `yy` - Copy entire line
* `p` - Paste after cursor

### Clipboard Operations
* `"+y` - Copy to system clipboard (works on all platforms)
* `"+p` - Paste from system clipboard (works on all platforms)

### Change Case
* `~` - Change case of character under cursor
* `g~w` - Change case of word

### Undo/Redo
* `u` - Undo last change
* `Ctrl + r` - Redo last undone change
* `.` - To repeat last command

## Text Objects and Operators

These commands work with operators: `c` (change), `d` (delete), `y` (copy), and `v` (select).

### Text Objects
* `iw` / `aw` - Inside word / around word with whitespace
* `i"` / `a"` - Inside quotes / including quotes
* `i{` / `a{` - Inside braces / including braces
* `i(` / `a(` - Inside parens / including parens
* `it` / `at` - Inside tags / including tags
* `ip` / `ap` - Inside paragraph / including blank lines

### Motion Commands
* `t"` - Till next double quote (cursor before character)
* `t}` - Till closing curly brace (cursor before character)
* `t)` - Till closing parenthesis (cursor before character)
* `t;` - Till semicolon (cursor before character)
* `f"` - To next double quote (cursor on character)
* `f}` - To closing curly brace (cursor on character)
* `f)` - To closing parenthesis (cursor on character)
* `f;` - To semicolon (cursor on character)

### Examples
* `cit` - Change text inside HTML tags
* `dap` - Delete paragraph with blank lines
* `yi"` - Copy text inside quotes
* `va{` - Select code block with braces
* `ct"` - Change text up to quote
* `df)` - Delete up to and including `)`

## Search and Navigation

### Search and Replace
* `/` - Start search
* `*` - Search for word under cursor
* `n` - Next search result
* `N` - Previous search result
* `:%s/old/new/g` - Replace all occurrences of 'old' with 'new'

### Code Navigation
* `gd` - Go to definition
* `gf` - Go to file
* `zc` - Fold (collapse) under cursor
* `zo` - Open fold under cursor

## Window Management and Exiting

### Window Management
* `:sp` - Split window horizontally
* `:vsp` - Split window vertically

### Exiting
* `:x` - Save and quit
* `:q!` - Quit without saving
