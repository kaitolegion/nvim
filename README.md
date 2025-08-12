# nvim
This is my neovim configurations 2025 resources and learnings


### What is neovim 

According to ChatGPT - Neovim is basically a modernized, supercharged text editor that’s based in Vim but redesigned and improved by developers based on their experience.

## Installations

- MacOS
```
brew install neovim
git clone https://github.com/LazyVim/starter ~/.config/nvim
rm -rf ~/.config/nvim/.git
```

## Neovim Essential Commands
A quick reference guide to essential Neovim commands for file management, navigation, editing, searching, and window management.

- File management
| Command        | Description              |
|----------------|--------------------------|
| `:e filename`  | Open a file              |
| `:w`           | Save file                |
| `:w filename`  | Save as (write to file)  |
| `:q`           | Quit                     |
| `:wq`          | Save and quit            |
| `:q!`          | Quit without saving      |
| `:x`           | Save and quit (like `:wq`)|
| `:e .`         | Open file explorer       |

---
-- navigation
| Command      | Description                  |
|--------------|------------------------------|
| `h` / `l`    | Move left / right            |
| `j` / `k`    | Move down / up               |
| `0`          | Move to start of line        |
| `^`          | Move to first non-blank char |
| `$`          | Move to end of line          |
| `gg`         | Go to start of file          |
| `G`          | Go to end of file            |
| `Ctrl + d`   | Scroll half-page down        |
| `Ctrl + u`   | Scroll half-page up          |

---
-- editing
| Command | Description          |
|---------|----------------------|
| `i`     | Insert before cursor |
| `a`     | Insert after cursor  |
| `o`     | Open new line below  |
| `O`     | Open new line above  |
| `x`     | Delete character     |
| `dd`    | Delete whole line    |
| `yy`    | Copy (yank) whole line |
| `p`     | Paste after cursor   |
| `P`     | Paste before cursor  |
| `u`     | Undo                 |
| `Ctrl + r` | Redo              |

---
-- search & replace
| Command            | Description                        |
|--------------------|----------------------------------|
| `/word`            | Search forward for “word”         |
| `?word`            | Search backward for “word”        |
| `n`                | Repeat search in same direction   |
| `N`                | Repeat search in opposite direction |
| `:%s/old/new/g`    | Replace all `old` with `new`      |
| `:s/old/new/g`     | Replace in current line            |

---
-- Windows & splits
| Command             | Description                      |
|---------------------|--------------------------------|
| `:sp filename`      | Horizontal split with file      |
| `:vsp filename`     | Vertical split with file        |
| `Ctrl + w` + `w`    | Switch between windows          |
| `Ctrl + w` + `q`    | Close current split             |
| `Ctrl + w` + `h/j/k/l` | Move to left/down/up/right split |

---

## Configurations

### Ctrl-s: keymap
Face issue when editing and save the file forcing you to normal mode with this configuration we can ctrl+s without bring back to normal mode.

```sh
-- step 1: goto 
nvim ~/.config/nvim/lua/config/keymaps.lua

-- step 2: enter this code
vim.keymap.set({ "n", "v" }, "<C-s>", "<cmd>w<CR>", { desc = "Save file" })
vim.keymap.set("i", "<C-s>", "<C-o>:w<CR>", { desc = "Save file" })

-- step 3: save 
:source %
-- step 4: restart
:qall
```

## Follow me
- Facebook <fb.me/kaitocoding>
