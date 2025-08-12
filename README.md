# nvim
This is my neovim configurations 2025 resources and learnings


### What is neovim 

According to ChatGPT - Neovim is basically a modernized, supercharged text editor that’s based in Vim but redesigned and improved by developers based on their experience.

## Installations

### enable save without bring back to normal mode



```sh
-- Save with Ctrl-s in any mode
vim.keymap.set({ "n", "v" }, "<C-s>", "<cmd>w<CR>", { desc = "Save file" })
vim.keymap.set("i", "<C-s>", "<C-o>:w<CR>", { desc = "Save file" })
```





## Follow me
- Facebook <fb.me/kaitocoding>
