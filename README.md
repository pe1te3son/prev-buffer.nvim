# prev-buffer.nvim

A simple Neovim plugin to switch to previous buffer with tab inspired by Spacemacs.

## Features

- Switch to the last buffer with fallback logic
- Delete current buffer and automatically switch to the previous buffer
- Prevents deleting modified buffers without saving
- Customizable keymaps

## Installation

### Using lazy.nvim

```lua
return { "pe1te3son/prev-buffer.nvim" }
```

## Configuration

### Default keymaps

- `<leader>bd` - Delete current buffer and switch to previous
- `<leader><Tab>` - Switch to last previous

### Custom configuration

```lua
return {
  "pe1te3son/prev-buffer.nvim",
  opts = {
    delete_key = "<leader>bd",  -- Custom delete buffer keymap
    switch_key = "<leader><Tab>", -- Custom switch buffer keymap
  },
}
```

## API

The plugin exposes the following functions:

- `require("prev-buffer").delete_current_buffer()` - Delete current buffer and switch to last.
  When deleting a buffer it should always use this function
  otherwise it will not switch to the last buffer correctly
- `require("prev-buffer").switch_to_last_buffer()` - Switch to last buffer
- `require("prev-buffer").setup(opts)` - Setup the plugin with options

## License

MIT
