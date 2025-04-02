---
Title: lazy.nvim setup - config function
Description: |
  lazy.nvim setup - config function
Tags:
  - neovim
  - lua
---

```lua
  config = function()
    local conform = require("conform")

    conform.setup({})
  end,
```
