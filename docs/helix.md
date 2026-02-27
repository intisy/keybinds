### Helix Keybindings

Helix is a post-modern, terminal-based text editor inspired by Vim and Kakoune. It uses a **selection-first** model: you select text first, then apply an action (the reverse of Vim's verb-then-motion). Helix has built-in LSP support, Treesitter integration, and multi-cursor editing out of the box with no plugins needed.

#### **Core Concepts**

*   **Modes:**
    *   **Normal:** The default mode for navigation and selection. **Press `Esc` to return here.**
    *   **Insert:** For typing text.
    *   **Select:** Similar to Normal but extends the selection with every motion.
    *   **Command (`:`):** For running commands.
*   **Selection-First:** In Vim you type `d3w` (delete 3 words). In Helix you type `3wd` (select 3 words, then delete). You always see what you're about to act on.

#### **The Absolute Essentials**

*   **Enter Insert Mode:** `i` (before cursor), `a` (after cursor), `I` (start of line), `A` (end of line), `o` (new line below), `O` (new line above).
*   **Return to Normal Mode:** `Esc`.
*   **Undo/Redo:** `u` (undo), `U` (redo).
*   **Save (`:w`):** Write the file.
*   **Quit (`:q`):** Quit. `:q!` to quit without saving. `:wq` to save and quit.

#### **Movement**

*   **Basic:** `h` (left), `j` (down), `k` (up), `l` (right).
*   **Word:** `w` (next word start), `b` (previous word start), `e` (word end).
*   **Line:** `0` (line start), `^` (first non-blank), `$` (line end).
*   **File:** `gg` (file start), `ge` (file end), `:` + line number (go to line).
*   **Page:** `Ctrl+d` (half page down), `Ctrl+u` (half page up), `Ctrl+f` (page down), `Ctrl+b` (page up).
*   **Matching Bracket:** `mm` (jump to matching bracket).
*   **Paragraph:** `[p` / `]p` (previous/next paragraph).
*   **Function:** `[f` / `]f` (previous/next function).

#### **Selection**

*   **Select Mode (v):** Enter select mode. All motions extend the selection.
*   **Select Line (x):** Select the entire current line. Press again for more lines.
*   **Expand Selection (Alt+Up):** Expand selection to the parent syntax node (Treesitter-aware).
*   **Shrink Selection (Alt+Down):** Shrink selection to the child syntax node.
*   **Select All (%):** Select the entire file.
*   **Select Inside (mi):** Select inside a pair (e.g., `mi(` selects inside parentheses).
*   **Select Around (ma):** Select around a pair (e.g., `ma"` selects including quotes).
*   **Split Selection (S):** Split the selection on a regex pattern, creating multiple selections.
*   **Keep Selections (K):** Keep only selections matching a regex.
*   **Remove Selections (Alt+K):** Remove selections matching a regex.

#### **Multi-Cursor**

*   **Add Cursor Below (C):** Add a cursor on the next line (with the same selection width).
*   **Add Cursor Above (Alt+C):** Add a cursor on the previous line.
*   **Split Selection to Lines (Alt+s):** Split a multi-line selection into individual line selections.
*   **Select All Matches (Ctrl+a):** Select all occurrences of the current selection in the file.
*   **Keep Primary (,):** Collapse to the primary cursor only.
*   **Cycle Primary (Alt+,):** Cycle through which cursor is the primary one.
*   **Remove Primary (Alt+.):** Remove the primary selection.

#### **Editing**

*   **Delete Selection (d):** Delete the selected text.
*   **Change Selection (c):** Delete the selected text and enter Insert mode.
*   **Yank/Copy (y):** Copy the selection.
*   **Paste After (p):** Paste after the cursor.
*   **Paste Before (P):** Paste before the cursor.
*   **Replace (r):** Replace the selection with a character.
*   **Indent (>):** Indent the selection.
*   **Unindent (<):** Unindent the selection.
*   **Toggle Comment (Ctrl+c):** Comment or uncomment the selection.
*   **Join Lines (J):** Join selected lines.
*   **Toggle Case (~):** Toggle the case of the selection.
*   **Repeat Last Change (.):** Repeat the last insertion or edit.

#### **Search**

*   **Search Forward (/):** Search for a regex pattern.
*   **Search Backward (?):** Search backward.
*   **Next Match (n):** Go to the next match.
*   **Previous Match (N):** Go to the previous match.
*   **Select Next Match (*):** Add the next match to the selections.
*   **Search for Selection (Ctrl+s):** Use the current selection as the search pattern.

#### **Space Menu**

Press `Space` in Normal mode to open the space menu:

*   **Space f:** File picker (fuzzy find files).
*   **Space F:** File picker (current directory).
*   **Space b:** Buffer picker (switch between open files).
*   **Space s:** Symbol picker (jump to symbols in the file).
*   **Space S:** Workspace symbol picker.
*   **Space g:** Live grep (search across files).
*   **Space d:** Diagnostics picker.
*   **Space a:** Code actions.
*   **Space r:** Rename symbol.
*   **Space h:** Hover documentation.
*   **Space k:** Show signature help.

#### **Window Management**

*   **Split Right (Ctrl+w v):** Vertical split.
*   **Split Down (Ctrl+w s):** Horizontal split.
*   **Focus (Ctrl+w h/j/k/l):** Move focus between splits.
*   **Close Window (Ctrl+w q):** Close the current split.
*   **Swap Window (Ctrl+w x):** Swap the current window with the next.

#### **Customization**

*   **Config File:** `~/.config/helix/config.toml`
*   **Languages File:** `~/.config/helix/languages.toml` (configure LSP servers per language).
*   **Example Config:**
    ```toml
    theme = "catppuccin_mocha"

    [editor]
    line-number = "relative"
    mouse = true
    bufferline = "multiple"
    auto-save = true

    [editor.cursor-shape]
    insert = "bar"
    normal = "block"
    select = "underline"

    [editor.indent-guides]
    render = true

    [keys.normal]
    C-s = ":w"
    C-q = ":q"
    ```
*   **No Plugin System:** Helix intentionally has no plugin system. All features (LSP, Treesitter, fuzzy finder, multi-cursor) are built in.
