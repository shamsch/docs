# VS Code Ninja

This outlines list of useful shortcuts in VS Code, `settings.json`, and `keybindings.json` that I use.

## Shortcuts

### Command Navigation

| Action                | Mac           | Windows        | Comment |
| --------------------- | ------------- | -------------- | ------- |
| Open command palette  | `cmd+shift+p` | `ctrl+shift+p` |         |
| Quick file navigation | `cmd+p`       | `ctrl+p`       |         |

### Interface Navigation

| Action                                         | Mac            | Windows         | Comment                    |
| ---------------------------------------------- | -------------- | --------------- | -------------------------- |
| Focus editor                                   | `cmd+1`        | `ctrl+1`        | also `shift+e` from custom |
| Toggle sidebar                                 | `control+q`    | `ctrl+q`        |                            |
| Move directly to explorer/ or back to editor   | `cmd+shift+e`  | `ctrl+shift+e`  |                            |
| Create a new editor group                      | `cmd+\`        | `ctrl+\`        |                            |
| Move focus to other editor sideway or vertical | `cmd+2,3,4...` | `ctrl+2,3,4...` |                            |
| Go between active files in editor              | `control+tab`  | `ctrl+tab`      |                            |
| Hide/Show explorer                             | `cmd+b`        | `ctrl+b`        |                            |

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

| Action                                     | Mac                        | Windows                     | Comment               |
| ------------------------------------------ | -------------------------- | --------------------------- | --------------------- |
| Find across all files                      | `cmd+shift+f`              | `ctrl+shift+f`              |                       |
| Find in files                              | `cmd+f`                    | `ctrl+f`                    |                       |
| To view result in editor area after search | `alt+enter`                | `option+enter`              | mac one is unverified |
| Toggle replace                             | `cmd+option+f`             | `ctrl+h`                    |                       |
| Go up and down search results              | `cmd+down` and then `down` | `ctrl+down` and then `down` |                       |
| Replace one                                | `cmd+Enter`                | `Enter`                     |                       |
| Replace all                                | `cmd+option+Enter`         | `Alt+Enter`                 |                       |
| Comment out line                           | `cmd+/`                    | `ctrl+/`                    |                       |
| Rename symbol i.e variables, fn            | `F2`                       | `F2`                        |                       |
| Find symbol in file                        | `cmd+t`                    | `ctrl+t`                    |                       |
| Peek definition                            | `F12`                      | `F12`                       |                       |

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
    },
  ],
  "vim.visualModeKeyBindingsNonRecursive": [
    {
      "before": ["d"],
      "after": ["\"", "_", "d"]
    },
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
    // github copilot toggle => space a i
    {
        "key": "space a i",
        "command": "github.copilot.completions.toggle",
        "when": "vim.mode == 'Normal'"
    },

    // VIM stuff remapped here

    // because $, *, and g_ is difficult to reach
    {
        "key": "space h",
        "command": "vim.remap",
        "when": "vim.mode == 'Normal'",
        "args": {
            "after": [
                "^"
            ]
        }
    },
    {
        "key": "space l",
        "command": "vim.remap",
        "when": "vim.mode == 'Normal'",
        "args": {
            "after": [
                "g",
                "_"
            ]
        }
    },
    {
        "key": "space f",
        "command": "vim.remap",
        "when": "vim.mode == 'Normal'",
        "args": {
            "after": [
                "*"
            ]
        }
    },
    // scroll down and center the cursor
    {
        "key": "space j",
        "command": "vim.remap",
        "when": "vim.mode == 'Normal' || vim.mode == 'Visual' || vim.mode == 'VisualLine'",
        "args": {
            "after": [
                "<C-d>",
                "z",
                "z"
            ]
        }
    },
    {
        "key": "space k",
        "command": "vim.remap",
        "when": "vim.mode == 'Normal' || vim.mode == 'Visual' || vim.mode == 'VisualLine'",
        "args": {
            "after": [
                "<C-u>",
                "z",
                "z"
            ]
        }
    },
    
    // BINDINGS INSPIRED FROM THIS GIST ON GITHUB
    // https://gist.github.com/nikolovlazar/1174876ab2769c52ac9fc1534c557d70
    
    // STARTS HERE
    
    // --- NAVIGATION ---
    // focus previous tab at the left => shift+j
    {
        "key": "shift+j",
        "command": "workbench.action.previousEditor",
        "when": "vim.mode == 'Normal'"
    },
    // focus next tab at the right => shift+k
    {
        "key": "shift+k",
        "command": "workbench.action.nextEditor",
        "when": "vim.mode == 'Normal'"
    },
    // go to left split => control+h
    {
        "key": "ctrl-h",
        "command": "workbench.action.navigateLeft"
    },
    // go to right split => control+l
    {
        "key": "ctrl-l",
        "command": "workbench.action.navigateRight"
    },
    // go to top split => control+k
    {
        "key": "ctrl-k",
        "command": "workbench.action.navigateUp"
    },
    // go to bottom split => control+j
    {
        "key": "ctrl-j",
        "command": "workbench.action.navigateDown"
    },
    // open all active editor => space , (comma)
    {
        "key": "space ,",
        "command": "workbench.action.showAllEditors",
        "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus)"
    },
    // toggle explorer sidebar and focus => space e
    {
        "key": "space e",
        "command": "runCommands",
        "args": {
            "commands": [
                "workbench.action.toggleSidebarVisibility",
                "workbench.files.action.focusFilesExplorer"
            ]
        },
        "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus) && !sideBarFocus"
    },
    {
        "key": "space e",
        "command": "runCommands",
        "args": {
            "commands": [
                "workbench.action.toggleSidebarVisibility",
                "workbench.action.focusActiveEditorGroup"
            ]
        },
        "when": "sideBarFocus && !inputFocus"
    },
    {
        "key": "space e",
        "when": "vim.mode == 'Normal' && editorTextFocus && foldersViewVisible",
        "command": "workbench.action.toggleSidebarVisibility"
    },

    // --- EXPLOERE ---
    // rename a file => r
    {
        "key": "r",
        "command": "renameFile",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // copy a file with => c
    {
        "key": "c",
        "command": "filesExplorer.copy",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // paste a file with => p
    {
        "key": "p",
        "command": "filesExplorer.paste",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // cut a file with => x
    {
        "key": "x",
        "command": "filesExplorer.cut",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // delete a file with => d
    {
        "key": "d",
        "command": "deleteFile",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // create a new file with => a
    {
        "key": "a",
        "command": "explorer.newFile",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // create a new folder with => shift+a
    {
        "key": "shift+a",
        "command": "explorer.newFolder",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // split to bottom => s
    {
        "key": "s",
        "command": "explorer.openToSide",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
    },
    // split to the left => shift+s
    {
        "key": "shift-s",
        "command": "runCommands",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus",
        "args": {
            "commands": [
                "workbench.action.splitEditorLeft",
                "explorer.openAndPassFocus",
                "workbench.action.closeOtherEditors"
            ]
        }
    },
    // open a file with => enter
    {
        "key": "enter",
        "command": "explorer.openAndPassFocus",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && !explorerResourceIsFolder && !inputFocus"
    },
    // unfold a folder within the explorer with => enter
    {
        "key": "enter",
        "command": "list.toggleExpand",
        "when": "filesExplorerFocus && foldersViewVisible && !explorerResourceIsRoot && explorerResourceIsFolder && !inputFocus"
    },

    // --- CODING ---
    // open code action => space c a
    {
        "key": "space c a",
        "command": "editor.action.codeAction",
        "when": "vim.mode == 'Normal' && editorTextFocus"
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
        "when": "vim.mode == 'Normal' && editorTextFocus"
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
    // quick open aka ctrl+p => space space
    {
        "key": "space space",
        "command": "workbench.action.quickOpen",
        "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus)"
    },
    // close all buffers/editors => space b a
    {
        "key": "space b a",
        "command": "workbench.action.closeAllEditors",
        "when": "(vim.mode == 'Normal' && editorTextFocus) || !inputFocus"
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
    // --- TERMINAL ---
    // toggle terminal panel => space t t
    {
        "key": "space t t",
        "command": "workbench.action.togglePanel",
        "when": "vim.mode == 'Normal' && (editorTextFocus || panelFocus || !inputFocus)"
    },
    // terminal kill => space t x
    {
        "key": "space t x",
        "command": "workbench.action.terminal.kill",
        "when": "vim.mode == 'Normal' && terminalFocus"
    },
    // create new terminal instance => space t n
    {
        "key": "space t n",
        "command": "workbench.action.terminal.new",
        "when": "vim.mode == 'Normal' && (editorTextFocus || panelFocus || !inputFocus)"
    },
    // go to next terminal => space t j
    {
        "key": "space t j",
        "command": "workbench.action.terminal.focusNext",
        "when": "vim.mode == 'Normal' && terminalFocus"
    },
    // go to prev terminal => space t k
    {
        "key": "space t k",
        "command": "workbench.action.terminal.focusPrevious",
        "when": "vim.mode == 'Normal' && terminalFocus"
    },
    // maximize/minimize terminal => space t m
    {
        "key": "space t m",
        "command": "workbench.action.toggleMaximizedPanel",
        "when": "vim.mode == 'Normal' && (editorTextFocus || !inputFocus || terminalFocus)"
    },

    // END HERE

    // OTHER KEYBINDINGS
]
```
