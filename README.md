# Neovim and LazyVim Guide

## What is Neovim?

Neovim is a modern text editor based on Vim. It is extremely fast, customizable,
and is controlled almost completely from the keyboard. It does not use a mouse by default.

## What is LazyVim?

LazyVim is a pre-built configuration for Neovim that includes:
- Plugin manager (lazy.nvim)
- Automatic autocompletion
- Syntax highlighting (treesitter)
- Search and navigation (Telescope, fzf-lua)
- LSP support (Language Server Protocol) for multiple languages
- Icons and color scheme

---

## Neovim modes

Neovim has different modes. Each mode has a function:

| Mode       | What it is for                          | How to enter   |
|------------|-----------------------------------------|----------------|
| Normal     | Navigate and edit text (default)        | `ESC`          |
| Insert     | Type text                               | `i`            |
| Visual     | Select text                             | `v`, `V`, `Ctrl+v` |
| Command    | Run commands                            | `:`            |

**IMPORTANT**: Always press `ESC` to return to Normal mode.

---

## Keyboard Shortcuts - LazyVim

### FILES

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `Space + f + f`    | Search file (Telescope)              |
| `Space + f + r`    | Open recent file                     |
| `Space + f + s`    | Save file (Save)                     |
| `Space + f + d`    | Delete file                          |
| `Space + f + n`    | Create new file                      |
| `Space + b + b`    | Search between buffers (tabs)        |
| `Space + b + d`    | Close current buffer                 |
| `Space + b + l`    | Next buffer                          |
| `Space + b + h`    | Previous buffer                      |

### BASIC NAVIGATION

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `h`                | Move left                            |
| `j`                | Move down                            |
| `k`                | Move up                              |
| `l`                | Move right                           |
| `w`                | Next word                            |
| `b`                | Previous word                        |
| `0`                | Start of line                        |
| `^`                | First non-blank character            |
| `$`                | End of line                          |
| `gg`               | Start of file                        |
| `G`                | End of file                          |
| `Ctrl + o`         | Go back to previous position         |
| `Ctrl + i`         | Go to next position                  |

### EDITING

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `i`                | Insert before the cursor             |
| `I`                | Insert at start of line              |
| `a`                | Insert after the cursor              |
| `A`                | Insert at end of line                |
| `o`                | New line below                       |
| `O`                | New line above                       |
| `x`                | Delete character                     |
| `dd`               | Delete whole line                    |
| `dw`               | Delete word                          |
| `d$`               | Delete to end of line                |
| `d0`               | Delete to start of line              |
| `D`                | Delete to end of line                |
| `cc`               | Change line (delete and enter Insert mode) |
| `cw`               | Change word                          |
| `C`                | Change to end of line                |
| `s`                | Delete character and type            |
| `S`                | Delete line and type                 |
| `r`                | Replace a character                  |
| `R`                | Replace mode (replace multiple)      |
| `u`                | Undo                                 |
| `Ctrl + r`         | Redo                                 |
| `.`                | Repeat last command                  |

### SELECTION (Visual Mode)

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `v`                | Select character                     |
| `V`                | Select whole line                    |
| `Ctrl + v`         | Select block/rectangle               |
| `d` or `x`         | Delete selection                     |
| `y`                | Copy selection (yank)                |
| `>`                | Indent selection                     |
| `<`                | Unindent selection                   |
| `=`                | Auto-indent selection                |
| `~`                | Toggle uppercase/lowercase           |

### COPY AND PASTE

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `y`                | Copy (yank)                          |
| `yy`               | Copy whole line                      |
| `yw`               | Copy word                            |
| `y$`               | Copy to end of line                  |
| `p`                | Paste after the cursor               |
| `P`                | Paste before the cursor              |

### SEARCH AND REPLACE

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `/`                | Search forward                       |
| `?`                | Search backward                      |
| `n`                | Next result                          |
| `N`                | Previous result                      |
| `*`                | Search word under cursor             |
| `:%s/old/new/g`    | Replace everywhere in the file       |
| `:s/old/new/g`     | Replace in the current line          |

### WINDOWS (Splits)

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `Space + w + w`    | Next window                          |
| `Space + w + d`    | Close window                         |
| `Space + w + s`    | Split horizontal                     |
| `Space + w + v`    | Split vertical                       |
| `Ctrl + h`         | Move to left window                  |
| `Ctrl + j`         | Move to window below                 |
| `Ctrl + k`         | Move to window above                 |
| `Ctrl + l`         | Move to right window                 |
| `Space + e`        | File explorer (Neo-tree)             |

### TABS

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `Shift + h`        | Previous tab                         |
| `Shift + l`        | Next tab                             |
| `Space + b + n`    | New tab                              |
| `Space + b + c`    | Close tab                            |

### LSP (Autocompletion and Errors)

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `gd`               | Go to definition                     |
| `gr`               | Search references                    |
| `gi`               | Go to implementation                 |
| `K`                | Show documentation                   |
| `<Space + ca>`     | Code actions                         |
| `<Space + cr>`     | Rename variable/symbol               |
| `<Space + cf`      | Format file                          |
| `<Space + cd`      | Show diagnostic errors               |
| `[d`               | Previous error                       |
| `]d`               | Next error                           |

### TELESCOPE (Advanced Search)

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `Space + f + f`    | Search file                          |
| `Space + f + g`    | Search in content (grep)             |
| `Space + f + b`    | Search in open buffers               |
| `Space + f + h`    | Search in history                    |
| `Space + f + r`    | Search recent file                   |
| `Space + s + s`    | Search word in the project           |
| `Space + s + g`    | Search in the current file           |

### GIT (Lazygit)

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `Space + g + g`    | Open Lazygit                         |
| `Space + g + b`    | View blame (who changed what)        |
| `Space + g + d`    | View file diff                       |
| `Space + g + h`    | View file history                    |
| `]h`               | Next git change                      |
| `[h`               | Previous git change                  |

### FILE EXPLORER (Neo-tree)

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `Space + e`        | Open/close explorer                  |
| `a`                | Create file or folder                |
| `d`                | Delete file or folder                |
| `r`                | Rename                               |
| `Enter`            | Open file                            |
| `Ctrl + s`         | Open in horizontal split             |
| `Ctrl + v`         | Open in vertical split               |
| `x`                | Close tree node                      |

### INTEGRATED TERMINAL

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `Space + f + t`    | Open floating terminal               |
| `Escape`           | Exit the terminal                    |

### MISC

| Shortcut           | Action                               |
|--------------------|--------------------------------------|
| `Space + h + h`    | Show/hide help                       |
| `Space + u`        | Change history (undo tree)           |
| `Space + L`        | LazyVim info                         |
| `Space + L + l`    | View LazyVim log                     |
| `Space + L + s`    | Sync plugins                         |
| `Ctrl + c`         | Cancel command                       |
| `:`                | Open command line                    |
| `:q`               | Close window                         |
| `:q!`              | Close without saving                 |
| `:wq`              | Save and close                       |
| `:w`               | Save                                 |

---

## Useful LazyVim Commands

### Plugin Management

| Command                    | Action                           |
|----------------------------|----------------------------------|
| `:Lazy`                    | Open plugin manager              |
| `:Lazy sync`               | Sync plugins                     |
| `:Lazy install`            | Install missing plugins          |
| `:Lazy update`             | Update all plugins               |
| `:Lazy clean`              | Remove unused plugins            |

### LSP Management

| Command                    | Action                           |
|----------------------------|----------------------------------|
| `:Mason`                   | Open LSP tool manager            |
| `:LspInfo`                 | View active LSPs                 |
| `:LspRestart`              | Restart LSP                      |

### Treesitter

| Command                    | Action                           |
|----------------------------|----------------------------------|
| `:TSInstall <language>`    | Install parser for a language    |
| `:TSUpdate`                | Update parsers                   |
| `:TSInstallInfo`           | View installed parsers           |

---

## Basic Workflow

### Open a file

```
Space + f + f     -> Search file -> Type name -> Enter
```

### Edit a file

```
1. Open file with Space + f + f
2. Navigate with h/j/k/l
3. Press i to enter Insert mode
4. Type code
5. Press ESC to return to Normal
6. Save with Space + f + s or :w
```

### Search text

```
Space + f + g     -> Type text to search -> Enter
Use Ctrl + n/p to navigate results
Enter to go to the result
```

### Copy and paste

```
1. Position the cursor
2. v to select (or V for whole line)
3. Move the cursor to select
4. y to copy
5. Position where the text will be pasted
6. p to paste
```

### Rename a variable

```
1. Position the cursor over the variable
2. Space + cr
3. Type the new name
4. Enter
```

---

## Tips for Beginners

1. **Avoid the mouse** - Perform all actions with the keyboard
2. **Master the basics first** - h/j/k/l, i, ESC, :w, :q
3. **Use visual mode** - v, V, Ctrl+v to select text
4. **Practice with vimtutor** - Run `vimtutor` in the terminal
5. **Save frequently** - Space + f + s or :w at short intervals
6. **Undo changes safely** - The `u` command allows reverting edits
7. **Use the explorer** - Space + e to view the files
8. **Search with Telescope** - Space + f + f is the most useful shortcut to locate files
9. **Search and replace** - / to search, :s/ to replace
10. **Practice consistently** - Spend approximately 30 minutes daily

---

## Common Errors and Solutions

| Error                          | Solution                         |
|--------------------------------|----------------------------------|
| Cannot exit Neovim             | Press ESC, type :q!              |
| Cannot type                    | Press i for Insert mode          |
| The file is not saved          | :w to save                       |
| Cannot find a file             | Space + f + f to search          |
| There are errors in the code   | Space + c + d to view errors     |
| Plugins do not load            | :Lazy sync to sync               |
| No autocompletion              | Check LSP with :LspInfo          |

---

## Resources

- `vimtutor` in the terminal (official Vim tutorial)
- `:help` in Neovim for built-in help
- LazyVim documentation: `:h lazyvim`
- Neovim docs: `:h` followed by the topic
