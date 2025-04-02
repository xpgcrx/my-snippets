---
Title: lazy.nvim setup - add keymaps
Description: |
  lazy.nvim setup - add keymaps
Tags:
  - neovim
  - lua
---

```lua
  keys = {
    {
      "<leader>ng",
      function()
        require("neogen").generate()
      end,
      desc = "Generate docs template(Neogen)",
      mode = "n",
    },
  },
```
