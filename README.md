# prev-manager.nvim

A simple Neovim plugin to switch to previous buffer with tab inspired by Spacemacs.

## Features

- Switch to the last buffer with fallback logic
- Delete current buffer and automatically switch to the previous buffer
- Prevents deleting modified buffers without saving
- Customizable keymaps

## Installation

### Using lazy.nvim

```lua
return {
  "pe1te3son/prev-buffer.nvim",
  version = "*", -- Use latest stable release
  keys = {
    { "<leader>bd", desc = "Delete current buffer and switch to previous" },
    { "<leader><Tab>", desc = "Switch to last previous" },
  },
  opts = {},
}
```

## Configuration

### Default keymaps

- `<leader>bd` - Delete current buffer and switch to previous
- `<leader><Tab>` - Switch to last previous

### Custom configuration

```lua
return {
  "pe1te3son/prev-buffer.nvim",
  version = "*", -- Use latest stable release
  opts = {
    delete_key = "<leader>bd",  -- Custom delete buffer keymap;
    switch_key = "<leader><Tab>", -- Custom switch buffer keymap
  },
}
```

## API

The plugin exposes the following functions:

- `require("prev-manager").delete_current_buffer()` - Delete current buffer and switch to last
- `require("prev-manager").switch_to_last_buffer()` - Switch to last buffer
- `require("prev-manager").setup(opts)` - Setup the plugin with options

## License

MIT
