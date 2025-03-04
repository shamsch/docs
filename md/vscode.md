# VS Code Ninja

This outlines list of useful shortcuts in VS Code, `settings.json`, and `keybindings.json` that I use. 

## Shortcuts
### Command Navigation
| Action | Mac | Windows |
|--------|-----|---------|
| Open command palette | `cmd+shift+p` | `cntrl+shift+p` |
| Quick file navigation | `cmd+p` | `cntrl+p` |

### Interface Navigation
| Action | Mac | Windows |
|--------|-----|---------|
| Focus editor | `cmd+1` | `cntrl+1` |
| Toggle sidebar | `cntrl+q` | `cntrl+q` |
| Move focus to editor below | `` | `` |
| Go between active files in editor | `control+tab` | `ctrl+tab` |

### Terminal Operations
| Action | Mac | Windows |
|--------|-----|---------|
| Open terminal | `cmd+backtick` | `cntrl+backtick` |
| Open new terminal | `cmd+shift+backtick` | `cntrl+shift+backtick` |
| Move between multiple terminals | `cmd+shift+[` and `cmd+shift+]` | `ctrl+shift+[` and `ctrl+shift+]` |

### Editor Operations
| Action | Mac | Windows |
|--------|-----|---------|
| Move line up | `option+up` | `alt+up` |
| Move line down | `option+down` | `alt+down` |
| Set multiple cursors | `option+click` | `alt+click` |
| Close active editor | `cmd+w` | `` |
| Close all editors | `` | `` |

### File Operations
| Action | Mac | Windows |
|--------|-----|---------|
| Create a new file in explorer | `option+n` | `alt+n` |
| Create a new folder in explorer | `option+shift+n` | `alt+shift+n` |

### Search and Replace
| Action | Mac | Windows |
|--------|-----|---------|
| Find across all files | `cmd+shift+f` | `cntrl+shift+f` |
| Find in files | `cmd+shift+f` | `cntrl+shift+f` |
| Toggle replace | `` | `ctrl+h` |
| Go up and down search results | `cmd`+`down` |`cntrl`+`down`|
| Replace one | `cmd+Enter` | `Enter` |
| Replace all | `cmd+Alt+Enter` | `Alt+Enter` |

### GitHub Copilot
| Action | Mac | Windows |
|--------|-----|---------|
| Open GitHub Copilot chat | `cmd+control+i` | `ctrl+alt+i` |
| Open GitHub Copilot editor | `cmd+shift+i` | `ctrl+shift+i` |
## Settings
``
	// SELF SET SETTINGS
	// JS and TS settings
	"javascript.updateImportsOnFileMove.enabled": "always", // Automatically updates imports when JavaScript files are moved
	"typescript.updateImportsOnFileMove.enabled": "always", // Automatically updates imports when TypeScript files are moved

	// Git settings
	"git.autofetch": true, // Automatically fetches changes from the remote repository
	"git.confirmSync": false, // Disables confirmation dialog for Git sync
	"git.enableSmartCommit": true, // Commit all changes when no files are added/staged for commit

	// Editor settings
	"editor.defaultFormatter": "esbenp.prettier-vscode", // Sets the default formatter for the editor
	"editor.fontFamily": "JetBrains Mono", // Sets the editor font family
	"editor.fontLigatures": true, // Disables font ligatures
	"editor.fontSize": 16, // Sets the editor font size
	"editor.minimap.enabled": false, // Disables the minimap
	"workbench.editor.openSideBySideDirection": "down", // Opens editors side by side in a downward direction
	"workbench.sideBar.location": "right",
	"explorer.confirmDelete": false, // Disables delete confirmation in the explorer
	"files.autoSave": "afterDelay", // Automatically saves files after a delay
	"diffEditor.ignoreTrimWhitespace": false, // Does not ignore trim whitespace in the diff editor
	"terminal.integrated.fontFamily": "monospace",
	"workbench.colorTheme": "Visual Studio Dark",
	"workbench.startupEditor": "none", // Sets the terminal font family:

	// VIM settings
	"vim.incsearch": true, // incremental search - does search as you type
	"vim.hlsearch": true, // highlight search - stop using :noh
	"vim.foldfix": true, // prevents fold to unfold when moving with hjkl
	// override for window to not conflict
	"vim.handleKeys": {
		"<C-c>": false, //copy
		"<C-v>": false, //paste
		"<C-x>": false, // cut
		"<C-z>": false, // undo
		"<C-p>": false, // files
		"<C-f>": false, // find
		"<C-a>": false, // select all
		"<C-q>": false, // navigate
	},
	"vim.leader": "<space>", // leader key
	// because $ and g_ is difficult to reach for start and end of line
	"vim.normalModeKeyBindingsNonRecursive": [
		{
		"before": ["<leader>", "h"],
		"after": ["^"]
		},
		{
		"before": ["<leader>", "l"],
		"after": ["g", "_"]
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
		}
	],
	// highlight yanked text
	"vim.highlightedyank.enable": true,
	"vim.highlightedyank.color": "yellow",
	"vim.highlightedyank.duration": 250,
	// relative lines
	"editor.lineNumbers": "relative",

	// OTHER AUTO GENERATED SETTINGS
	"github.copilot.selectedCompletionModel": "gpt-4o-copilot",
	"github.copilot.enable": {
		"*": true,
		"plaintext": false,
		"markdown": true,
		"scminput": false
	},
``

## Keybindings
``
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
    
    // OTHER KEYBINDINGS 
]
``