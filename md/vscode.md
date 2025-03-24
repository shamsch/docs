# VS Code Ninja

This outlines list of useful shortcuts in VS Code, `settings.json`, and `keybindings.json` that I use.

## Shortcuts

### Command Navigation

| Action                | Mac           | Windows        | Comment |
| --------------------- | ------------- | -------------- | ------- |
| Open command palette  | `cmd+shift+p` | `ctrl+shift+p` |         |
| Quick file navigation | `cmd+p`       | `ctrl+p`       |         |

### Interface Navigation

| Action                                         | Mac            | Windows         | Comment |
| ---------------------------------------------- | -------------- | --------------- | ------- |
| Focus editor                                   | `cmd+1`        | `ctrl+1`        |         |
| Toggle sidebar                                 | `control+q`    | `ctrl+q`        |         |
| Move directly to explorer/ or back to editor   | `cmd+shift+e`  | `ctrl+shift+e`  |         |
| Create a new editor group                      | `cmd+\`        | `ctrl+\`        |         |
| Move focus to other editor sideway or vertical | `cmd+2,3,4...` | `ctrl+2,3,4...` |         |
| Go between active files in editor              | `control+tab`  | `ctrl+tab`      |         |
| Hide/Show explorer                             | `cmd+b`        | `ctrl+b`        |         |

### Terminal Operations

| Action                          | Mac                             | Windows                     | Comment                                       |
| ------------------------------- | ------------------------------- | --------------------------- | --------------------------------------------- |
| Open terminal                   | `cmd+backtick`                  | `ctrl+backtick`             |                                               |
| Open new terminal               | `cmd+shift+backtick`            | `ctrl+shift+backtick`       |                                               |
| Move between multiple terminals | `cmd+shift+[` and `cmd+shift+]` | `ctrl+pgup` and `ctrl+pgdn` | overriden with custom `keybinding.json` below |

### Editor Operations

| Action                                   | Mac            | Windows     | Comment              |
| ---------------------------------------- | -------------- | ----------- | -------------------- |
| Move line up                             | `option+up`    | `alt+up`    |                      |
| Move line down                           | `option+down`  | `alt+down`  |                      |
| Select current word and subsequent words | `cmd+d`        | `ctrl+d`    |                      |
| Set multiple cursors                     | `option+click` | `alt+click` |                      |
| Close active editor                      | `cmd+w`        | `ctrl+f4`   | overriden in windows |
| Close all editors                        | `cmd+k w`      | `ctrl+k w`  |                      |
| Preview markdown file                    | `cmd+k v`      | `ctrl+k v`  |                      |

### File Operations

| Action                          | Mac              | Windows       | Comment |
| ------------------------------- | ---------------- | ------------- | ------- |
| Create a new file in explorer   | `option+n`       | `alt+n`       |         |
| Create a new folder in explorer | `option+shift+n` | `alt+shift+n` |         |

### Search and Replace

| Action                          | Mac                        | Windows                     | Comment |
| ------------------------------- | -------------------------- | --------------------------- | ------- |
| Find across all files           | `cmd+shift+f`              | `ctrl+shift+f`              |         |
| Find in files                   | `cmd+f`                    | `ctrl+f`                    |         |
| Toggle replace                  | `cmd+option+f`             | `ctrl+h`                    |         |
| Go up and down search results   | `cmd+down` and then `down` | `ctrl+down` and then `down` |         |
| Replace one                     | `cmd+Enter`                | `Enter`                     |         |
| Replace all                     | `cmd+option+Enter`         | `Alt+Enter`                 |         |
| Comment out line                | `cmd+/`                    | `ctrl+/`                    |         |
| Rename symbol i.e variables, fn | `F2`                       | `F2`                        |         |
| Find symbol in file             | `cmd+t`                    | `ctrl+t`                    |         |
| Peek definition                 | `F12`                      | `F12`                       |         |

### GitHub Copilot

| Action                     | Mac             | Windows        | Comment |
| -------------------------- | --------------- | -------------- | ------- |
| Open GitHub Copilot chat   | `cmd+control+i` | `ctrl+alt+i`   |         |
| Open GitHub Copilot editor | `cmd+shift+i`   | `ctrl+shift+i` |         |

## Settings

```json
{
  // SELF SET SETTINGS

  // JS and TS settings
  "javascript.updateImportsOnFileMove.enabled": "always", // Automatically updates imports when JavaScript files are moved
  "typescript.updateImportsOnFileMove.enabled": "always", // Automatically updates imports when TypeScript files are moved

  // Git settings
  "git.autofetch": true, // Automatically fetches changes from the remote repository
  "git.enableSmartCommit": true, // Commit all changes when no files are added/staged for commit
  "git.confirmSync": false, // Does not ask for confirmation before syncing changes

  // Editor settings
  "editor.fontFamily": "JetBrains Mono", // Sets the editor font family
  "editor.fontLigatures": true, // Disables font ligatures
  "editor.fontSize": 16, // Sets the editor font size
  "editor.suggestSelection": "first", // Automatically selects the first suggestion when pressing Tab
  "editor.tabCompletion": "on", // Enables tab completion
  "editor.tabSize": 4, // Sets the tab size to 4 spaces
  "editor.wordWrap": "on", // Enables word wrap
  "editor.minimap.enabled": false, // Disables the minimap
  "editor.bracketPairColorization.enabled": true, // Enables bracket pair colorization
  "workbench.editor.openSideBySideDirection": "down", // Opens editors side by side in a downward direction
  "workbench.sideBar.location": "right",
  "workbench.editor.enablePreview": false,
  "workbench.editor.enablePreviewFromQuickOpen": false, // stops replacing the current file with a newly opened file
  "files.autoSave": "afterDelay", // Automatically saves files after a delay
  "diffEditor.ignoreTrimWhitespace": false, // Does not ignore trim whitespace in the diff editor
  "terminal.integrated.fontFamily": "JetBrains Mono", // Sets the terminal font family
  "workbench.colorTheme": "Visual Studio Dark",
  "workbench.startupEditor": "none", // Sets the terminal font family
  "editor.renderWhitespace": "all", // Renders all whitespace characters in the editor with dots and dashes
  "explorer.confirmDelete": false, // Disables the confirmation dialog when deleting files
  "explorer.confirmDragAndDrop": false, // Disables the confirmation dialog when deleting files
  "security.workspace.trust.untrustedFiles": "open", // Just open files

  // VIM settings
  "vim.incsearch": true, // incremental search - does search as you type
  "vim.hlsearch": true, // highlight search - stop using :noh
  "vim.foldfix": true, // prevents fold to unfold when moving with hjkl
  // Only allows Ctrl+I, Ctrl+O, and Ctrl+R for Vim while preserving all other VSCode shortcuts
  "vim.useCtrlKeys": false, // Globally disable all Ctrl key combinations for Vim
  "vim.handleKeys": {
    "<C-i>": true, // Jump to newer position in jump list
    "<C-o>": true, // Jump to older position in jump list
    "<C-r>": true // Redo or paste from register in insert mode
  },
  "vim.leader": "<space>", // leader key
  "vim.normalModeKeyBindingsNonRecursive": [
    // because $, *, and g_ is difficult to reach
    {
      "before": ["<leader>", "h"],
      "after": ["^"]
    },
    {
      "before": ["<leader>", "l"],
      "after": ["g", "_"]
    },
    {
      "before": ["<leader>", "f"],
      "after": ["*"]
    },
    // d should not copy to register, hence prefixed
    {
      "before": ["d"],
      "after": ["\"", "_", "d"]
    },
    // focus previous tab at the left
    {
      "before": ["J"],
      "commands": ["workbench.action.previousEditor"]
    },
    // focus next tab at the right
    {
      "before": ["K"],
      "commands": ["workbench.action.nextEditor"]
    },
    // overrides vim from taking over and retains vscode's default behavior for ctrl+d
    {
      "before": ["<C-d>"],
      "commands": ["editor.action.addSelectionToNextFindMatch"]
    },
    // scroll up and down and center the cursor
    {
      "before": ["<leader>", "d"],
      "after": ["<C-d>", "z", "z"]
    },
    {
      "before": ["<leader>", "u"],
      "after": ["<C-u>", "z", "z"]
    }
  ],
  "vim.visualModeKeyBindingsNonRecursive": [
    {
      "before": ["<leader>", "h"],
      "after": ["^"]
    },
    {
      "before": ["<leader>", "l"],
      "after": ["g", "_"]
    },
    {
      "before": ["<leader>", "f"],
      "after": ["*"]
    },
    {
      "before": ["d"],
      "after": ["\"", "_", "d"]
    },
    {
      "before": ["J"],
      "commands": ["workbench.action.previousEditor"]
    },
    {
      "before": ["K"],
      "commands": ["workbench.action.nextEditor"]
    },
    {
      "before": ["<C-d>"],
      "commands": ["editor.action.addSelectionToNextFindMatch"]
    },
    {
      "before": ["<leader>", "d"],
      "after": ["<C-d>", "z", "z"]
    },
    {
      "before": ["<leader>", "u"],
      "after": ["<C-u>", "z", "z"]
    }
  ],
  "vim.operatorPendingModeKeyBindingsNonRecursive": [
    // this is make space+l or h to work with yank/cut/delete
    {
      "before": ["<leader>", "h"],
      "after": ["^"]
    },
    {
      "before": ["<leader>", "l"],
      "after": ["g", "_"]
    }
  ],
  // highlight yanked text
  "vim.highlightedyank.enable": true,
  "vim.highlightedyank.color": "yellow",
  "vim.highlightedyank.duration": 250,
  // relative lines for easy traversal i.e 10j or 33k
  "editor.lineNumbers": "relative",

  // OTHER AUTO GENERATED SETTINGS
  "github.copilot.enable": {
    "*": true,
    "plaintext": false,
    "markdown": true,
    "scminput": false
  },
  "security.workspace.trust.untrustedFiles": "open",
}
```

## Keybindings

```json
[
  // SELF SET KEYBINDINGS
  {
    "key": "shift+alt+n",
    "command": "explorer.newFolder"
  },
  {
    "key": "alt+n",
    "command": "explorer.newFile"
  },
  {
    "key": "ctrl+pageup",
    "command": "workbench.action.terminal.focusPrevious",
    "when": "terminalFocus"
  },
  {
    "key": "ctrl+pagedown",
    "command": "workbench.action.terminal.focusNext",
    "when": "terminalFocus"
  },
  {
    "key": "alt+j",
    "command": "workbench.action.toggleMaximizedPanel"
  },
  // OTHER KEYBINDINGS
]
```
