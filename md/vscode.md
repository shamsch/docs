# VS Code Ninja

This outlines list of useful shortcuts in VS Code, `settings.json`, and `keybindings.json` that I use.

## Shortcuts

### Command Navigation

| Action                | Mac           | Windows        | Custom          |
| --------------------- | ------------- | -------------- | --------------- |
| Open command palette  | `cmd+shift+p` | `ctrl+shift+p` | `space space >` |
| Quick file navigation | `cmd+p`       | `ctrl+p`       | `space space `  |

### Interface Navigation

| Action                                         | Mac            | Windows         | Custom                  |
| ---------------------------------------------- | -------------- | --------------- | ----------------------- |
| Focus editor                                   | `cmd+1`        | `ctrl+1`        | `control/ctrl + h`      |
| Toggle sidebar                                 | `control+q`    | `ctrl+q`        | `space e`               |
| Move directly to explorer/ or back to editor   | `cmd+shift+e`  | `ctrl+shift+e`  | `space e`               |
| Create a new editor group                      | `cmd+\`        | `ctrl+\`        | `:sp`                   |
| Move focus to other editor sideway or vertical | `cmd+2,3,4...` | `ctrl+2,3,4...` | `control/ctrl+h,j,k,l`  |
| Go between active files in editor              | `control+tab`  | `ctrl+tab`      | `shift+j` and `shift+k` |
| Hide/Show explorer                             | `cmd+b`        | `ctrl+b`        | `space e`               |

### Terminal Operations

| Action                          | Mac                             | Windows                     | Custom                                        |
| ------------------------------- | ------------------------------- | --------------------------- | --------------------------------------------- |
| Open terminal                   | `cmd+backtick`                  | `ctrl+backtick`             |                                               |
| Open new terminal               | `cmd+shift+backtick`            | `ctrl+shift+backtick`       |                                               |
| Move between multiple terminals | `cmd+shift+[` and `cmd+shift+]` | `ctrl+pgup` and `ctrl+pgdn` | overriden with custom `keybinding.json` below |

### Editor Operations

| Action                                   | Mac            | Windows        | Comment          |
| ---------------------------------------- | -------------- | -------------- | ---------------- |
| Move line up                             | `option+up`    | `alt+up`       |                  |
| Move line down                           | `option+down`  | `alt+down`     |                  |
| Select current word and subsequent words | `cmd+d`        | `ctrl+d`       | `ctrl/control+n` |
| Set multiple cursors                     | `option+click` | `alt+click`    |                  |
| Close active editor                      | `cmd+w`        | `ctrl+f4`      | `space b x`      |
| CLose all but active editor              | `cmd+option+w` | `ctrl+shift+w` | `space b a`      |
| Close all editors                        | `cmd+k w`      | `ctrl+k w`     | `space b o`      |
| Preview markdown file                    | `cmd+k v`      | `ctrl+k v`     |                  |

### File Operations

| Action                          | Mac              | Windows          | Custom    |
| ------------------------------- | ---------------- | ---------------- | --------- |
| Create a new file in explorer   | `option+n`       | `alt+n`          | `n`       |
| Create a new folder in explorer | `option+shift+n` | `alt+shift+n`    | `shift+n` |
| Delete a file in explorer       | `cmd+backspace`  | `ctrl+backspace` | `d`       |
| Rename a file in explorer       | `enter`          | `enter`          | `r`       |
| Open a file from explorer       | `space`          | `space`          | `enter`   |

### Search and Replace

| Action                                     | Mac                        | Windows                     | Custom      |
| ------------------------------------------ | -------------------------- | --------------------------- | ----------- |
| Find across all files                      | `cmd+shift+f`              | `ctrl+shift+f`              | `space s g` |
| Find in files                              | `cmd+f`                    | `ctrl+f`                    | `space s l` |
| To view result in editor area after search | `cmd+enter`                | `ctrl+enter`                |             |
| Toggle replace                             | `cmd+option+f`             | `ctrl+h`                    |             |
| Go up and down search results              | `cmd+down` and then `down` | `ctrl+down` and then `down` |             |
| Replace one                                | `cmd+Enter`                | `Enter`                     |             |
| Replace all                                | `cmd+option+Enter`         | `Alt+Enter`                 |             |
| Comment out line                           | `cmd+/`                    | `ctrl+/`                    |             |
| Rename symbol i.e variables, fn            | `F2`                       | `F2`                        | `space c r` |
| Find symbol in file                        | `cmd+t`                    | `ctrl+t`                    |             |
| Peek definition                            | `F12`                      | `F12`                       |             |

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
  "git.autofetch": true, // Automatically FETCHES changes from the remote repository
  "git.enableSmartCommit": true, // Commit all changes when no files are added/staged for commit
  "git.confirmSync": false, // Does not ask for confirmation before syncing changes

  // Editor settings
  "editor.fontFamily": "JetBrains Mono", // Sets the editor font family
  "editor.fontLigatures": true, // Disables font ligatures
  "editor.fontSize": 16, // Sets the editor font size
  "editor.suggestSelection": "first", // Automatically selects the first suggestion when pressing Tab
  "editor.tabCompletion": "on", // Enables tab completion
  "editor.tabSize": 4, // Sets the tab size to 4 spaces
  "editor.minimap.enabled": false, // Disables the minimap
  "editor.bracketPairColorization.enabled": true, // Enables bracket pair colorization
  "workbench.editor.openSideBySideDirection": "down", // Opens editors side by side in a downward direction
  "workbench.sideBar.location": "right",
  "workbench.editor.enablePreview": false,
  "workbench.editor.enablePreviewFromQuickOpen": false, // stops replacing the current file with a newly opened file
  "files.autoSave": "afterDelay", // Automatically saves files after a delay
  "diffEditor.ignoreTrimWhitespace": false, // Does not ignore trim whitespace in the diff editor
  "terminal.integrated.fontFamily": "JetBrains Mono",
  "terminal.integrated.suggest.enabled": true, // Enables suggestions in the integrated terminal
  "workbench.startupEditor": "none", // Sets the terminal font family
  "editor.renderWhitespace": "all", // Renders all whitespace characters in the editor with dots and dashes
  "explorer.confirmDelete": false, // Disables the confirmation dialog when deleting files
  "explorer.confirmDragAndDrop": false, // Disables the confirmation dialog when deleting files
  "security.workspace.trust.untrustedFiles": "open", // Just open files
  "workbench.activityBar.location": "top", // keep explorer, source control, find etc. on top like Cursor
  "workbench.layoutControl.enabled": false, // removes unused stuff from top

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
  // "vim.leader": "", // leader key
  "vim.normalModeKeyBindingsNonRecursive": [
    // d should not copy to register, hence prefixed
    {
      "before": ["d"],
      "after": ["\"", "_", "d"]
    }
  ],
  "vim.visualModeKeyBindingsNonRecursive": [
    {
      "before": ["d"],
      "after": ["\"", "_", "d"]
    }
  ],
  // highlight yanked text
  "vim.highlightedyank.enable": true,
  "vim.highlightedyank.color": "yellow",
  "vim.highlightedyank.duration": 250,
  // relative lines for easy traversal i.e 10j or 33k
  "editor.lineNumbers": "relative",
  //search
  "search.searchOnType": true,
  "search.searchEditor.focusResultsOnSearch": true,

  // OTHER AUTO GENERATED SETTINGS
  "github.copilot.enable": {
    "*": true,
    "plaintext": false,
    "markdown": true,
    "scminput": false,
    "javascriptreact": true,
    "go": true
  },
  "[javascriptreact]": {
    "editor.defaultFormatter": "vscode.typescript-language-features"
  }
}
```

## Keybindings

```json
[
  // SELF SET KEYBINDINGS
  // terminal stuff
  // move between tabs in terminal
  {
    "key": "alt+k",
    "command": "workbench.action.terminal.focusPrevious",
    "when": "terminalFocus"
  },
  {
    "key": "alt+j",
    "command": "workbench.action.terminal.focusNext",
    "when": "terminalFocus"
  },
  // kill a terminal
  {
    "key": "alt+x",
    "command": "workbench.action.terminal.kill",
    "when": "terminalFocus"
  },
  // new terminal
  {
    "key": "alt+n",
    "command": "workbench.action.terminal.new",
    "when": "terminalFocus"
  },
  // split a terminal
  {
    "key": "alt+\\",
    "command": "workbench.action.terminal.split",
    "when": "terminalFocus"
  },
  // move between the splits
  {
    "key": "alt+h",
    "command": "workbench.action.terminal.focusPreviousPane",
    "when": "terminalFocus"
  },
  {
    "key": "alt+l",
    "command": "workbench.action.terminal.focusNextPane",
    "when": "terminalFocus"
  },
  //make terminal full screen
  {
    "key": "alt+f",
    "args": {
      "commands": [
        "workbench.action.toggleMaximizedPanel",
        "workbench.action.closeSidebar"
      ]
    },
    "command": "runCommands",
    "when": "terminalFocus"
  },
  // toggle terminal from anywhere
  {
    "key": "alt+t",
    "args": {
      "commands": [
        "workbench.action.terminal.toggleTerminal",
        "workbench.action.closeSidebar"
      ]
    },
    "command": "runCommands",
  },
  // VIM stuff remapped here
  // because $, *, and g_ is difficult to reach
  {
    "args": {
      "after": [
        "^",
        "x"
      ]
    },
    "command": "vim.remap",
    "key": "space h",
    "when": "vim.mode == 'Normal' && editorTextFocus "
  },
  {
    "args": {
      "after": [
        "g",
        "_"
      ]
    },
    "command": "vim.remap",
    "key": "space l",
    "when": "vim.mode == 'Normal' && editorTextFocus"
  },
  {
    "args": {
      "after": [
        "*"
      ]
    },
    "command": "vim.remap",
    "key": "space f",
    "when": "vim.mode == 'Normal' && editorTextFocus"
  },
  // scroll down and center the cursor
  {
    "args": {
      "after": [
        "<C-d>",
        "z",
        "z"
      ]
    },
    "command": "vim.remap",
    "key": "space j",
    "when": "(vim.mode == 'Normal' || vim.mode == 'Visual' || vim.mode == 'VisualLine') && editorTextFocus"
  },
  {
    "args": {
      "after": [
        "<C-u>",
        "z",
        "z"
      ]
    },
    "command": "vim.remap",
    "key": "space k",
    "when": "(vim.mode == 'Normal' || vim.mode == 'Visual' || vim.mode == 'VisualLine') && editorTextFocus"
  },
  // BINDINGS INSPIRED FROM THIS GIST ON GITHUB
  // https://gist.github.com/nikolovlazar/1174876ab2769c52ac9fc1534c557d70
  // STARTS HERE
  // --- NAVIGATION ---
  // focus previous tab at the left => shift+j
  {
    "command": "workbench.action.previousEditor",
    "key": "shift-j",
    "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus)"
  },
  // focus next tab at the right => shift+k
  {
    "command": "workbench.action.nextEditor",
    "key": "shift-k",
    "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus)"
  },
  // go to left split => control+h
  {
    "command": "workbench.action.navigateLeft",
    "key": "ctrl-h",
    "when": "vim.mode == 'Normal'"
  },
  // go to right split => control+l
  {
    "command": "workbench.action.navigateRight",
    "key": "ctrl-l",
    "when": "vim.mode == 'Normal'"
  },
  // go to top split => control+k
  {
    "command": "workbench.action.navigateUp",
    "key": "ctrl-k",
    "when": "vim.mode == 'Normal'"
  },
  // go to bottom split => control+j
  {
    "command": "workbench.action.navigateDown",
    "key": "ctrl-j",
    "when": "vim.mode == 'Normal'"
  },
  // open all active editor => space , (comma)
  {
    "command": "workbench.action.showAllEditors",
    "key": "space ,",
    "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus)"
  },
  // toggle explorer sidebar and focus => space e
  {
    "args": {
      "commands": [
        "workbench.action.toggleSidebarVisibility",
        "workbench.files.action.focusFilesExplorer"
      ]
    },
    "command": "runCommands",
    "key": "space e",
    "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus) && !sideBarFocus"
  },
  {
    "args": {
      "commands": [
        "workbench.action.toggleSidebarVisibility",
        "workbench.action.focusActiveEditorGroup"
      ]
    },
    "command": "runCommands",
    "key": "space e",
    "when": "sideBarFocus && !inputFocus"
  },
  {
    "command": "workbench.action.toggleSidebarVisibility",
    "key": "space e",
    "when": "vim.mode == 'Normal' && editorTextFocus && foldersViewVisible"
  },
  // --- EXPLOERE ---
  // rename a file => r
  {
    "command": "renameFile",
    "key": "r",
    "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // copy a file with => c
  {
    "command": "filesExplorer.copy",
    "key": "c",
    "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // paste a file with => p
  {
    "command": "filesExplorer.paste",
    "key": "p",
    "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // cut a file with => x
  {
    "command": "filesExplorer.cut",
    "key": "x",
    "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // delete a file with => d
  {
    "command": "deleteFile",
    "key": "d",
    "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // create a new file with => a
  {
    "command": "explorer.newFile",
    "key": "a",
    "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // create a new folder with => shift+a
  {
    "command": "explorer.newFolder",
    "key": "shift+a",
    "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // open a file with => enter
  {
    "command": "explorer.openAndPassFocus",
    "key": "enter",
    "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceIsFolder && !inputFocus"
  },
  // unfold a folder within the explorer with => enter
  {
    "command": "list.toggleExpand",
    "key": "enter",
    "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && explorerResourceIsFolder && !inputFocus"
  },
  // --- CODING ---
  // open code action => space c a
  {
    "command": "editor.action.codeAction",
    "key": "space c a",
    "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus) && !suggestWidgetVisible"
  },
  // open code suggestion => space c s
  {
    "key": "space c s",
    "command": "editor.action.triggerSuggest",
    "when": "editorTextFocus && !editorHasSelection && !suggestWidgetVisible && vim.mode == 'Normal'"
  },
  // rename func, variable in code => space c r
  {
    "key": "space c r",
    "command": "editor.action.rename",
    "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus)"
  },
  // buffer/editor delete => space b x
  {
    "key": "space b x",
    "command": "workbench.action.closeActiveEditor",
    "when": "(vim.mode == 'Normal' && editorTextFocus) || !inputFocus"
  },
  // buffer/editor delete inactive or others => space b o
  {
    "key": "space b o",
    "command": "workbench.action.closeOtherEditors",
    "when": "(vim.mode == 'Normal' && editorTextFocus) || !inputFocus"
  },
  // close all buffers/editors => space b a
  {
    "key": "space b a",
    "command": "workbench.action.closeAllEditors",
    "when": "(vim.mode == 'Normal' && editorTextFocus) || !inputFocus"
  },
  // quick open aka ctrl+p => space space
  {
    "key": "space space",
    "command": "workbench.action.quickOpen",
    "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus)"
  },
  // go to definition but open aside => space g d
  {
    "key": "space g d",
    "command": "editor.action.revealDefinitionAside",
    "when": "vim.mode == 'Normal' && editorTextFocus"
  },
  // search globally => space s g
  {
    "key": "space s g",
    "command": "workbench.action.findInFiles",
    "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus)"
  },
  // search locally => space s l
  {
    "key": "space s l",
    "command": "actions.find",
    "when": "vim.mode == 'Normal' && editorTextFocus"
  },
  // open git => space g g
  {
    "key": "space g g",
    "command": "runCommands",
    "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus)",
    "args": {
      "commands": [
        "workbench.view.scm",
        "workbench.scm.focus"
      ]
    }
  },
  // next match => control+n
  {
    "key": "ctrl-n",
    "command": "editor.action.addSelectionToNextFindMatch",
    "when": "(vim.mode == 'Normal' || vim.mode == 'Visual') && (editorTextFocus || !inputFocus)"
  },
  // --- GitHub Copilot ---
  // github copilot toggle => space a i
  {
    "command": "github.copilot.completions.toggle",
    "key": "space a i",
    "when": "vim.mode == 'Normal' && editorTextFocus"
  }
  // END HERE
  // OTHER KEYBINDINGS
]
```
