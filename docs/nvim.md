## Neovim Keyboard Reference

Neovim is a modernized fork of Vim with built-in LSP support, Lua scripting, and a thriving plugin ecosystem. All standard Vim keybindings work in Neovim. This page focuses on Neovim-specific features and the most common plugin keybindings. For core Vim motions and editing commands, see the [Vim reference](vim.md).

#### **What's Different from Vim**

*   **Config File:** `~/.config/nvim/init.lua` (Lua) or `~/.config/nvim/init.vim` (Vimscript). Lua is the modern standard.
*   **Built-in Terminal:** Neovim has a first-class integrated terminal emulator.
*   **Built-in LSP Client:** Native Language Server Protocol support for code intelligence (completions, diagnostics, go-to-definition, etc.).
*   **Lua API:** Plugins and configuration are primarily written in Lua, offering better performance and ergonomics than Vimscript.
*   **Treesitter Integration:** Built-in support for tree-sitter, providing better syntax highlighting, code folding, and text objects.

#### **Built-in Terminal**

*   **Open Terminal (`:terminal` or `:term`):** Opens a terminal buffer.
*   **Enter Terminal Mode:** Press `i` or `a` in the terminal buffer to start typing commands.
*   **Exit Terminal Mode (`Ctrl+\ Ctrl+n`):** Returns to Normal mode from the terminal buffer.
*   **Split Terminal:**
    *   `:split | terminal`: Open terminal in a horizontal split.
    *   `:vsplit | terminal`: Open terminal in a vertical split.
*   **Common Mapping:**
    ```lua
    -- Toggle terminal with <leader>t
    vim.keymap.set('n', '<leader>t', ':split | terminal<CR>', { desc = 'Open terminal' })
    -- Easier escape from terminal mode
    vim.keymap.set('t', '<Esc><Esc>', '<C-\\><C-n>', { desc = 'Exit terminal mode' })
    ```

#### **Built-in LSP Keybindings**

These are not bound by default but are the community-standard mappings (set via `vim.lsp.buf` in your config):

*   **Go to Definition (`gd`):** Jump to the definition of the symbol under the cursor.
*   **Go to Declaration (`gD`):** Jump to the declaration.
*   **Go to Implementation (`gi`):** Jump to the implementation.
*   **Go to Type Definition (`gt`):** Jump to the type definition.
*   **Hover Documentation (`K`):** Show hover documentation for the symbol under the cursor.
*   **Signature Help (`Ctrl+k`):** Show function signature help while in Insert mode.
*   **Rename Symbol (`<leader>rn`):** Rename the symbol under the cursor across the project.
*   **Code Action (`<leader>ca`):** Show available code actions (quick fixes, refactors).
*   **Show Diagnostics (`<leader>d`):** Show diagnostics for the current line in a floating window.
*   **Next Diagnostic (`]d`):** Jump to the next diagnostic.
*   **Previous Diagnostic (`[d`):** Jump to the previous diagnostic.
*   **Format Buffer (`<leader>f`):** Format the current buffer using the LSP formatter.
*   **Show References (`gr`):** List all references to the symbol under the cursor.
*   **Example LSP Config:**
    ```lua
    vim.api.nvim_create_autocmd('LspAttach', {
      callback = function(ev)
        local opts = { buffer = ev.buf }
        vim.keymap.set('n', 'gd', vim.lsp.buf.definition, opts)
        vim.keymap.set('n', 'K', vim.lsp.buf.hover, opts)
        vim.keymap.set('n', '<leader>rn', vim.lsp.buf.rename, opts)
        vim.keymap.set('n', '<leader>ca', vim.lsp.buf.code_action, opts)
        vim.keymap.set('n', 'gr', vim.lsp.buf.references, opts)
        vim.keymap.set('n', '<leader>f', function()
          vim.lsp.buf.format { async = true }
        end, opts)
      end,
    })
    ```

#### **Treesitter Text Objects & Motions**

With `nvim-treesitter-textobjects`, you get syntax-aware motions:

*   **Select Function (`vaf` / `vif`):** Select around/inside a function.
*   **Select Class (`vac` / `vic`):** Select around/inside a class.
*   **Select Parameter (`vaa` / `via`):** Select around/inside a function parameter.
*   **Select Conditional (`vai`):** Select around a conditional block.
*   **Next Function Start (`]m`):** Jump to the start of the next function/method.
*   **Previous Function Start (`[m`):** Jump to the start of the previous function/method.
*   **Next Function End (`]M`):** Jump to the end of the next function/method.
*   **Previous Function End (`[M`):** Jump to the end of the previous function/method.

#### **Telescope (Fuzzy Finder)**

Telescope is the most popular fuzzy finder plugin. Common keybindings:

*   **Find Files (`<leader>ff`):** Fuzzy search for files in the project.
*   **Live Grep (`<leader>fg`):** Search for a string across all files (requires `ripgrep`).
*   **Buffers (`<leader>fb`):** List and switch between open buffers.
*   **Help Tags (`<leader>fh`):** Search Neovim help documentation.
*   **Recent Files (`<leader>fr`):** Browse recently opened files.
*   **Git Files (`<leader>gf`):** Fuzzy find files tracked by git.
*   **Inside Telescope:**
    *   `Ctrl+n` / `Ctrl+p`: Next/previous result.
    *   `Ctrl+x`: Open in horizontal split.
    *   `Ctrl+v`: Open in vertical split.
    *   `Ctrl+t`: Open in new tab.
    *   `Esc`: Close Telescope.

#### **File Explorer (nvim-tree / neo-tree)**

Common keybindings when a file tree plugin is installed:

*   **Toggle File Tree (`<leader>e`):** Open or close the file explorer sidebar.
*   **Inside the Tree:**
    *   `Enter` or `o`: Open file/directory.
    *   `a`: Create a new file or directory.
    *   `d`: Delete file/directory.
    *   `r`: Rename file/directory.
    *   `x`: Cut file.
    *   `c`: Copy file.
    *   `p`: Paste file.
    *   `R`: Refresh the tree.
    *   `H`: Toggle hidden files.
    *   `q`: Close the tree.

#### **Buffer & Window Management**

*   **Next Buffer (`]b` or `:bnext`):** Switch to the next buffer.
*   **Previous Buffer (`[b` or `:bprev`):** Switch to the previous buffer.
*   **Delete Buffer (`<leader>bd` or `:bdelete`):** Close the current buffer.
*   **Split Navigation (`Ctrl+h/j/k/l`):** Move between splits (common remapping of Vim's `Ctrl+w h/j/k/l`).
*   **Resize Splits:**
    *   `Ctrl+Up/Down`: Increase/decrease split height.
    *   `Ctrl+Left/Right`: Increase/decrease split width.

#### **Git Integration (vim-fugitive / gitsigns)**

*   **Git Status (`:Git` or `<leader>gs`):** Open the git status window (fugitive).
*   **Stage Hunk (`<leader>hs`):** Stage the hunk under the cursor (gitsigns).
*   **Undo Stage Hunk (`<leader>hu`):** Undo staging the hunk (gitsigns).
*   **Preview Hunk (`<leader>hp`):** Preview the diff of the hunk under the cursor.
*   **Next Hunk (`]c`):** Jump to the next changed hunk.
*   **Previous Hunk (`[c`):** Jump to the previous changed hunk.
*   **Blame Line (`<leader>gb`):** Show git blame for the current line.
*   **Diff View (`<leader>gd`):** Open a diff view of the current file.

#### **Completion (nvim-cmp)**

When an autocompletion plugin like `nvim-cmp` is active:

*   **Trigger Completion (`Ctrl+Space`):** Manually trigger the completion menu.
*   **Next Item (`Ctrl+n` or `Tab`):** Select the next completion item.
*   **Previous Item (`Ctrl+p` or `Shift+Tab`):** Select the previous completion item.
*   **Confirm Selection (`Enter` or `Ctrl+y`):** Accept the selected completion.
*   **Dismiss (`Ctrl+e`):** Close the completion menu.
*   **Scroll Docs (`Ctrl+d` / `Ctrl+u`):** Scroll through documentation in the completion popup.

#### **Diagnostics & Quickfix**

*   **Open Diagnostic Float (`<leader>d`):** Show the full diagnostic message in a floating window.
*   **Next Diagnostic (`]d`):** Jump to the next diagnostic.
*   **Previous Diagnostic (`[d`):** Jump to the previous diagnostic.
*   **Quickfix List (`:copen`):** Open the quickfix list window.
*   **Next Quickfix (`:cnext` or `]q`):** Go to the next quickfix item.
*   **Previous Quickfix (`:cprev` or `[q`):** Go to the previous quickfix item.
*   **Location List (`:lopen`):** Open the location list window (buffer-local quickfix).

#### **Customization**

*   **Config File:** `~/.config/nvim/init.lua`
*   **Plugin Manager:** Most users use `lazy.nvim` for plugin management.
*   **Setting Keymaps in Lua:**
    ```lua
    -- Basic keymap
    vim.keymap.set('n', '<leader>w', ':w<CR>', { desc = 'Save file' })

    -- With options
    vim.keymap.set('n', '<leader>q', ':q<CR>', { noremap = true, silent = true, desc = 'Quit' })

    -- Multiple modes
    vim.keymap.set({ 'n', 'v' }, '<leader>y', '"+y', { desc = 'Copy to clipboard' })
    ```
*   **Setting the Leader Key:**
    ```lua
    vim.g.mapleader = ' '       -- Space as leader key
    vim.g.maplocalleader = ','  -- Comma as local leader
    ```
*   **Starter Configurations:** If you want a pre-configured setup, consider:
    *   **kickstart.nvim**: Minimal, well-documented starting point.
    *   **LazyVim**: Full-featured distribution with sane defaults.
    *   **NvChad**: Fast, modular configuration with a nice UI.
    *   **AstroNvim**: Extensible, community-driven configuration.
