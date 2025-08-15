# buffer-manager.nvim

A simple Neovim plugin for intelligent buffer management inspired by Spacemacs.

## Features

- Switch to the last buffer with smart fallback logic
- Delete current buffer and automatically switch to the last buffer
- Prevents deleting modified buffers without saving
- Customizable keymaps

## Installation

### Using lazy.nvim

```lua
return {
  "peter/buffer-manager.nvim",
  keys = {
    { "<leader>bd", desc = "Delete current buffer and switch to last" },
    { "<leader><Tab>", desc = "Switch to last buffer" },
  },
  opts = {},
}
```

## Configuration

### Default keymaps

- `<leader>bd` - Delete current buffer and switch to last
- `<leader><Tab>` - Switch to last buffer

### Custom configuration

```lua
return {
  "peter/buffer-manager.nvim",
  opts = {
    delete_key = "<leader>bd",  -- Custom delete buffer keymap
    switch_key = "<leader><Tab>", -- Custom switch buffer keymap
  },
}
```

## API

The plugin exposes the following functions:

- `require("buffer-manager").delete_current_buffer()` - Delete current buffer and switch to last
- `require("buffer-manager").switch_to_last_buffer()` - Switch to last buffer
- `require("buffer-manager").setup(opts)` - Setup the plugin with options

## License

MIT