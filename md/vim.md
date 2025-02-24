# VIM motions I actually know and use

All of the following commands will work by default in any vim environment. I use them in VSCode primarly with occasional use in the terminal.

However, in VSCode, I like to make a few changes. Paste these to your `settings.json` file:

```json
{
    "vim.hlsearch": true,
    "vim.incsearch": true
}
```

> I also remap Caps Lock and Esc, but that's a system-wide setting.)

## Basic Navigation

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
* `gg` - Jump to beginning of file
* `G` - Jump to end of file

### Paragraph/Sentence Movement

* `]` or `[` - Move over paragraph
* `(` or `)` - Move over sentence

### Other Navigation

* `Ctrl + o` - Jump back to previous location
* `Ctrl + i` - Jump forward to next location
* `Ctrl + u` - Move half page up
* `Ctrl + d` - Move half page down

## Editing Commands

### Insert Mode

* `i` - Insert before cursor
* `a` - Insert after cursor
* `o` - Insert on new line below

### Delete/Change/Yank (Copy)

* `x` - Delete character under cursor
* `dw` - Delete word
* `dd` - Delete entire line
* `yw` - Copy word
* `yy` - Copy entire line
* `p` - Paste after cursor
* `"+y` or `"*y` - Copy to system
* `"+p` or `"*p` - Copy to system 

### Change Case

* `~` - Change case of character under cursor
* `g~w` - Change case of word

## Search and Replace

* `/` - Start search
* `*` - Search for word under cursor
* `n` - Next search result
* `N` - Previous search result
* `gd` - Go to definition
* `:%s/old/new/g` - Replace all occurrences of 'old' with 'new'

## Visual Mode

* `v` - Select character-wise
* `V` - Select line-wise
* `Ctrl-v` - Select block-wise
* `ggVG` - Select entire file
* `>>` - Indent selected text
* `<<` - Unindent selected text

## Text Objects and Till Commands

These commands work in conjunction with `c` (change), `d` (delete), `y` (copy), and `v` (select).

### Text Objects

* `iw` / `aw` - Inside word / including whitespace around word (`Hello` vs `|Hello`)
* `i"` / `a"` - Inside quotes / including quotes (`Hello` vs `"Hello"`)
* `i{` / `a{` - Inside braces / including braces (`x = 1` vs `{x = 1}`)
* `i(` / `a(` - Inside parens / including parens (`arg` vs `(arg)`)
* `it` / `at` - Inside tags / including tags (`text` vs `<div>text</div>`)
* `ip` / `ap` - Inside paragraph / including surrounding newlines

### Till Commands

* `t"` - Till double quote (`"Hello"` → `|Hello"`). Moves cursor before the next `"`
* `t}` - Till closing curly brace (`{x = 1}` → `{x = 1|}`). Moves cursor before the next `}`
* `t)` - Till closing parenthesis (`(arg)` → `(arg|)`. Moves cursor before the next `)`
* `t;` - Till semicolon (`int x = 10;` → `int x = 10|;`). Moves cursor before the next `;`

**Examples:**

* `cit` changes between `<div>text</div>` tags → `<div>|</div>`
* `dap` deletes paragraph including blank lines
* `yi"` copies inside `"Hello"` → `Hello`
* `va{` selects `{x = 1}` including braces
* `ct"` changes `"Hello"` to `"|"`
* `yt)` copies `arg` from `(arg)`
* `vt;` visually selects up to (but not including) the next semicolon.

## Undo/Redo

* `u` - Undo last change
* `Ctrl + r` - Redo last undone change

## Window Management

* `:sp` - Split window horizontally
* `:vsp` - Split window vertically

## Exiting

* `:x` - Save and quit
* `:q!` - Quit without saving

## Mode Switching

* `Esc` - Return to normal mode
