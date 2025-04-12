# VIM motions I actually know and use

All of the following commands will work by default in any vim environment. I use them in VSCode primarly with occasional use in the terminal.
However, in VSCode, I like to make a few changes. Find these changes with rest of my vscode settings [here](/docs/template.html?file=vscode.md#settings).

> I also remap Caps Lock to Esc, but that's a system-wide setting.

## I. Core Navigation

### Basic Cursor Movement
- `h` - Move cursor left
- `j` - Move cursor down
- `k` - Move cursor up
- `l` - Move cursor right

### Word Navigation
- `w` - Move to start of next word
- `b` - Move to beginning of current/previous word
- `e` - Move to end of word

### Line Navigation
- `^` - Jump to beginning of line (first non-blank character)
- `$` - Jump to end of line
- `g_` - Jump to end of line (last non-blank character)

### File Navigation
- `gg` - Jump to beginning of file
- `G` - Jump to end of file

## II. Advanced Navigation & Jumping

### By Code Structure
- `%` - Jump to matching bracket ({}, [], ())

### Semantic Navigation (Paragraphs/Sentences)
- `]` or `[` - Move over paragraph
- `(` or `)` - Move over sentence

### Screen Movement
- `Ctrl + u` or `pgup` - Move half page up
- `Ctrl + d` or `pgdn` - Move half page down

### Jump History
- `Ctrl + o` - Jump back to previous location
- `Ctrl + i` - Jump forward to next location

### Viewport Adjustment
- `zz` - Make the current line center of view

## III. Modes and Mode Switching

### Entering Normal Mode
- `Esc` - Return to normal mode

### Entering Insert Mode
- `i` - Insert before cursor
- `a` - Insert after cursor
- `o` - Insert on new line below

### Entering Visual Mode (Selection)
- `v` - Select character-wise
- `V` - Select line-wise

## IV. Basic Editing Operations

### Deleting Characters
- `x` - Delete character under cursor

### Replacing Characters
- `r` - to replace character under cursor

### Undo / Redo
- `u` - Undo last change
- `Ctrl + r` - Redo last undone change

### Repeat Last Command
- `.` - To repeat last command

## V. Operators, Motions, and Text Objects (The Vim Grammar)

*Core Concept: Editing often involves combining an **Operator** (`d` delete, `c` change, `y` yank/copy, `v` select visually) with a **Motion** or **Text Object**.*

### Using Motions with Operators (Examples)
- `dw` - Delete word
- `dd` - Delete entire line
- `yw` - Copy word
- `yy` - Copy entire line
*(These use operators `d` and `y` with motions `w` and the implicit line motion)*

### Text Objects
*Define blocks of text. Format: `[operator][i/a][object]` (`i`=inside, `a`=around).*
- `iw` / `aw` - Inside word / around word with whitespace
- `i"` / `a"` - Inside quotes / including quotes
- `i{` / `a{` - Inside braces / including braces
- `i(` / `a(` - Inside parens / including parens
- `it` / `at` - Inside tags / including tags
- `ip` / `ap` - Inside paragraph / including blank lines

### Targeted Motions (f / t)
*Move *to* or *till* a character on the current line.*
- `t"` - Till next double quote (cursor before character)
- `t}` - Till closing curly brace (cursor before character)
- `t)` - Till closing parenthesis (cursor before character)
- `t;` - Till semicolon (cursor before character)
- `f"` - To next double quote (cursor on character)
- `f}` - To closing curly brace (cursor on character)
- `f)` - To closing parenthesis (cursor on character)
- `f;` - To semicolon (cursor on character)
- `;` - press `;` to repeat last `f` or `t`

### Operator + Motion/Object Examples
- `cit` - Change text inside HTML tags (`c` operator + `it` text object)
- `dap` - Delete paragraph with blank lines (`d` operator + `ap` text object)
- `yi"` - Copy text inside quotes (`y` operator + `i"` text object)
- `va{` - Select code block with braces (`v` operator + `a{` text object)
- `ct"` - Change text up to quote (`c` operator + `t"` motion)
- `df)` - Delete up to and including `)` (`d` operator + `f)` motion)

## VI. Yanking, Pasting, and Registers

### Basic Yank/Paste
- `yw` - Copy word
- `yy` - Copy entire line
- `p` - Paste after cursor

### Viewing Registers
- `:reg` - Show yank registers aka clipboard
- `"0p` - Paste from yank register 0

### System Clipboard Interaction
- `"+y` - Copy to system clipboard (works on all platforms)
- `"+p` - Paste from system clipboard (works on all platforms)

## VII. Visual Mode Operations (Selection)

### Selecting the Whole File
- `ggVG` - Select entire file (Combines `gg`, `V`, `G`)

### Acting on Selections
- `>>` - Indent selected text
- `<<` - Unindent selected text

### Reselecting Last Selection
- `gv` - To reselect the last visual selection

## VIII. Search and Replace

### Searching
- `/` - Start search
- `*` - Search for word under cursor
- `n` - Next search result
- `N` - Previous search result

### Global Replace
- `:%s/old/new/g` - Replace all occurrences of 'old' with 'new'

## IX. Code-Specific Navigation & Folding

### Jumping
- `gd` - Go to definition
- `gf` - Go to file
- `m<character>` - to set mark
- `'<character>` - to go to mark 

### Displaying Information (VS Code Specific)
- `gh` - Open hoover (ONLY WORKS IN VS CODE)

### Folding
- `zc` - Fold (collapse) under cursor
- `zo` - Open fold under cursor

## X. Text Formatting & Case Manipulation

### Changing Case
- `~` - Change case of character under cursor
- `gUw` - Uppercase word
- `guw` - Lowercase word

### Formatting
- `gg=G` - Format whole file

## XI. Macros (Recording & Playback)

### Recording
- `q` + `<any_letter>` - Start recording while in normal mode
- `q` - Again to stop recording

### Playback
- `@` + `<that_letter>` - Play the recorded macro

## XII. Window Management

### Splitting Windows
- `:sp` - Split window horizontally
- `:vsp` - Split window vertically

## XIII. Saving and Exiting

### Common Exit Commands
- `:x` - Save and quit
- `:q!` - Quit without saving
