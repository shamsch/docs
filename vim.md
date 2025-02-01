# Practical Vim Shortcuts Reference Guide

## Navigation
### Basic Movement
- `h` - Move cursor left
- `j` - Move cursor down
- `k` - Move cursor up
- `l` - Move cursor right

### Line Navigation
- `^` - Jump to beginning of line
- `$` - Jump to end of line
- `gg` - Jump to beginning of file
- `G` - Jump to end of file

### Word Navigation
- `w` - Move to start of next word
- `b` - Move to beginning of current/previous word
- `e` - Move to end of word

## Search and Replace
- `/` - Start search
- `n` - Next search result
- `N` - Previous search result
- `:%s/old/new/g` - Replace all occurrences of 'old' with 'new'

## Editing
### Insert Mode
- `i` - Insert before cursor
- `a` - Insert after cursor
- `o` - Insert on new line below

### Delete and Modify
- `x` - Delete character under cursor
- `dd` - Cut entire line
- `yy` - Copy entire line
- `p` - Paste after cursor

### Undo/Redo
- `u` - Undo last change
- `Ctrl + r` - Redo last undone change

## Visual Mode
- `V` - Select current line
- `ggVG` - Select entire file
- `>` - Indent selected text
- `<` - Unindent selected text

## Window Management
- `:sp` - Split window horizontally
- `:vsp` - Split window vertically

## Exiting
- `:x` - Save and quit
- `:q!` - Quit without saving

## Mode Switching
- `Esc` or `Cmd + c` - Return to normal mode (from visual or insert mode)