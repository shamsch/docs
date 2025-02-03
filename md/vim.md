# Vim Motion I know and use

All of the following commands will work by default in any vim environment. I use them in VSCode primarly with occasional use in the terminal.

However, in VSCode, I like to make a few changes. Paste these to your settings.json file:

```json
    	// Vim settings
	"vim.hlsearch": true, // Highlights search results
	"vim.incsearch": true // Shows result as you search 
```

### Basic Movement

-   `h` - Move cursor left
-   `j` - Move cursor down
-   `k` - Move cursor up
-   `l` - Move cursor right
-   `]` or `[` - Move over paragraph (next new line without text)
-   `(` or `)` - Move over sentence 

### Line Navigation

-   `^` - Jump to beginning of line
-   `$` - Jump to end of line
-   `gg` - Jump to beginning of file
-   `G` - Jump to end of file

### Word Navigation

-   `w` - Move to start of next word
-   `b` - Move to beginning of current/previous word
-   `e` - Move to end of word

## Other navigational commands

-   `Ctrl + o` - Jump back to previous location
-   `Ctrl + i` - Jump forward to next location
-   `Ctrl + u` - Move half page up
-   `Ctrl + d` - Move half page down

## Search and Replace

-   `/` - Start search
-   `*` - Search for word under cursor
-   `n` - Next search result
-   `N` - Previous search result
-   `gd` - Go to definition 
-   `:%s/old/new/g` - Replace all occurrences of 'old' with 'new'

## Editing

### Insert Mode

-   `i` - Insert before cursor
-   `a` - Insert after cursor
-   `o` - Insert on new line below

### Delete and Modify

-   `x` - Delete character under cursor
-   `dw` - Delete wrod
-   `dd` - Delete entire line
-   `yw` - Copy word
-   `yy` - Copy entire line
-   `p` - Paste after cursor

### Nifty tricks
Text operations (use `c` to change, `d` to delete, `y` to copy, `v` to select):
* `iw` - Inside word (e.g. `ciw`, `yiw`)
* `i"` / `a"` - Inside quotes / including quotes (`Hello` vs `"Hello"`)
* `i{` / `a{` - Inside braces / including braces (`x = 1` vs `{x = 1}`)
* `i(` / `a(` - Inside parens / including parens (`arg` vs `(arg)`)
* `it` / `at` - Inside tags / including tags (`text` vs `<div>text</div>`)
* `ip` / `ap` - Inside paragraph / including surrounding newlines

For example:
* `cit` changes between `<div>text</div>` tags → `<div>|</div>`
* `dap` deletes paragraph including blank lines
* `yi"` copies inside `"Hello"` → `Hello`
* `va{` selects `{x = 1}` including braces

### Undo/Redo

-   `u` - Undo last change
-   `Ctrl + r` - Redo last undone change

## Visual Mode

-   `V` - Select current line
-   `ggVG` - Select entire file
-   `>` - Indent selected text
-   `<` - Unindent selected text

## Window Management

-   `:sp` - Split window horizontally
-   `:vsp` - Split window vertically

## Exiting

-   `:x` - Save and quit
-   `:q!` - Quit without saving

## Mode Switching

-   `Esc` - Return to normal mode (from visual or insert mode)
