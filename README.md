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
